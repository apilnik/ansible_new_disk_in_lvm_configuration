# ansible_new_disk_lvm_configuration
##### After adding a new disk to the virtual machine, it will automatically configure lvm.

###### Vars:
###### "vg_name" => Volume Group name like "appvg"
###### "lv_name" => Logical Volume name like "applv"
###### "lv_size" => Specify extents as a percentage of VG|PVS|FREE like "100%FREE"
###### "fs" => filesystem on lvm like "ext4"
###### "mount_point" => directory to mount the filesystem like "/app"
###### "mount_opts" => Options common to filesystem like "defaults,exec,noatime...."
##### Raw_device:
It will be chosen from ansible_devices when item.value.host.startswith('Serial') and (  item.value.partitions|length == 0) if VG is already exist LV will be extend.
