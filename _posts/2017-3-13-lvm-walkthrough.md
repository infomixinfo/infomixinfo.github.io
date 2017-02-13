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
 
 
 
 
