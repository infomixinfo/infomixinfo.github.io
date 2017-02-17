---  
layout: post
title: Create a network between VMs in Oracle VirtualHost
---
 Creating a network between 2 Oracle VirtualHost VMs will be handy for testing/learning topics such as Clustering,
 SAN, Load balancing etc.One way to connect the VMs is by using "Internal Network" Option.
 
 Please note that the when using "Internal Network" option you will not be able to connect to the host or Internet.
 For that you will have to enable NAT on the VMs.
 
 Go to network section on each VM and select "Internal Network" and give a network name as provided in the image.
 
 ![_config.yml]({{ site.baseurl }}/images/image001.png)
 
 Now configure each VM with a ip range in the same network.
 
 ![_config.yml]({{ site.baseurl }}/images/image002.png)
 
  
 
  

