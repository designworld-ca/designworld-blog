---
title: VmWare oddities
categories: [software, virtualization]
tags: [vmware]
---

# VmWare oddities
I have noticed that when my Esxi 6 server crashes unexpectedly due to a power outage when I reboot it half the virtual machines are not showing.

Turns out when you register a new vm you should also power it down, unregister and then reregister it.  That way the information is written to vmInventory.xml as opposed to being held in memory and flushed with an ungraceful shutdown.

Not classed as a feature or a bug....

[KB Article](https://kb.vmware.com/s/article/2013301)

 

