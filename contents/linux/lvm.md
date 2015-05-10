---
title: LVM
layout: page
permalink: linux/lvm/
---

= On SAN provided LUNs

== Creation of LVM volume from empty disk

If the disk has never been attached to the machine and has been hot-attached, run iscsi rescan and multipath reload:

[source, bash]
/usr/bin/rescan-scsi-bus.sh
/etc/init.d/multipathd reload

If you want to give an alias to the new LUN, run `multipath -ll` to see it's **WWID** and then edit the `/etc/multipath.conf` file accordingly.

[source, linux-config]
...
    multipath {
        wwid    ?????????????????????????????????
        alias   [ALIAS]
    }
...

If you have modified the `/etc/multipath.conf` file, remember to reload multipathd:

[source, bash]
/etc/init.d/multipathd reload

Create the *LVM Physical Volume*, the *LVM Volume Group* and the *LVM Logical Volume*

[source, bash]
pvcreate /dev/mapper/[ALIAS]
vgcreate vg_[ALIAS] /dev/mapper/[ALIAS]
vgchange -ay vg_[ALIAS]
lvcreate -l 100%FREE -n lv_[ALIAS] vg_[ALIAS]

If you are working on a LUN that could be seen by more than a machine, remember to Add the tags to prevent other machines to inadvertirely mount the drive you are working on.

[source, bash]
vgchange --addtag [YOUR_HOSTNAME] vg_[ALIAS]
lvchange --addtag [YOUR_HOSTNAME] /dev/vg_[ALIAS]/lv_[ALIAS]

NOTE: If you want ot check your tags, you can use:
    vgs -o name,tags
    lvs -o name,tags

To remove the tag from the volumes and logical volumes:

[source, bash]
vgchange --deltag [YOUR_HOSTNAME] vg_[ALIAS]
lvchange --deltag [YOUR_HOSTNAME] /dev/vg_[ALIAS]/lv_[ALIAS]

== Restore of LVM volume from the snapshot of another disk

