---  
layout: post
title: Setup SCSI target and initiaor
---
  
In storage Logical Unit Number(LUN) is a logical number used to identify a logical unit that can be accessed by iSCSI protocol.
The logical unit can be a hard disk or a portion of hard disk or an lvm partition. The computer that connects to the storage 
server to import the block device represented by the LUN id will be the initiator and the server which provides the block device 
will be the target.
  
