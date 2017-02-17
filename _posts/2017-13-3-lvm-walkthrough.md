---  
layout: post
title: Understanding lvm 
---
  
 These are the things that you should remember before proceeding.
 
 Physical volumes and physical disks or partitions.Using lvm multiple physical volumes 
 can be combined into volume groups.Logical volumes are virtual hard disks created from volume
 groups.
 
 As the first step create a 15GB disk in the VM.
 
 ![_config.yml]({{ site.baseurl }}/images/image003.png)
 
 Now create the extended partition.
 
 ![_config.yml]({{ site.baseurl }}/images/image004.png)
 
 Now create 3 logical partitions. Select +652 additional cylindes the first 2 partitions and the default value of 
 1958 for the the 3rd partition as shown in the below image. 652 cylinders has been taken to equally devide 
 the 3 logical partitions.
 
 ![_config.yml]({{ site.baseurl }}/images/image005.png)

 Now convert the logical partitions into lvm partitions using Hex code 8e. 
 
 ![_config.yml]({{ site.baseurl }}/images/image006.png)
 
 Then create the physical volume.
 
 ![_config.yml]({{ site.baseurl }}/images/image007.png)
 
 After that create the volme group using the first 2 disks from the physical volume. Volume group can be extended 
 later by adding the last disk. vgs command will show the size of the volume group and the number of physical volumes 
 that are part of the volume group.
 
 ![_config.yml]({{ site.baseurl }}/images/image008.png)
 
 Now create 2 logical volumes in the volume group. The first command with option -L will allocate 5GB where as the 
 second command with option -l gives the number of extents. It can also be expressed as a percentage of the total available 
 space as shown in the example. lvdisplay will list the logical volumes.
 
 ![_config.yml]({{ site.baseurl }}/images/image009.png)
 
 Now format the logical volume.
 
 ![_config.yml]({{ site.baseurl }}/images/image010.png)
 
 Mount the logical volume. Add the remaining physical volume to vg01 volume group using vgextend. Then extend the 
 logical volume with the available free space in the volume group using lvextend. This can be done while the logical volume
 is mounted. The changes will come into effect only after running the resize2fs command.
 
 ![_config.yml]({{ site.baseurl }}/images/image011.png)
 
 
 
 
 
