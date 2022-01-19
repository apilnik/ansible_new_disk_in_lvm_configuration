# new_disk_in_lvm_configuration
After adding a new disk to the virtual machine, it will help to configure lvm.

Vars:
"vg_name" => Volume Group name like "appvg"
"lv_name" => Logical Volume name like "applv"
"require_lv_size" => Specify extents as a percentage of VG|PVS|FREE like "100%FREE"
"fs" => filesystem on lvm like "ext4"
"mount_point" => directory to mount the filesystem like "/app"

Raw_device:
It will be chosen from ansible_devices when item.value.host.startswith('Serial') and (  item.value.partitions|length == 0)
 
 value:
      holders: []
      host: 'Serial Attached SCSI controller: VMware PVSCSI SCSI Controller (rev 02)'
      links:
        ids: []
        labels: []
        masters: []
        uuids: []
      model: Virtual disk
      partitions: {}
      removable: '0'
      rotational: '1'
      sas_address: null
      sas_device_handle: null
      scheduler_mode: deadline
      sectors: '20971520'
      sectorsize: '512'
      size: 10.00 GB
      support_discard: '0'
      vendor: VMware
      virtual: 1

