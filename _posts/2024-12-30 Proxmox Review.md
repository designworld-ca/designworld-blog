# Why didn't I do this sooner?

Having used VmWare's Esxi for so many years that my version went out of support I needed to upgrade or migrate.  
Broadcom's purchase of VmWare and the ensuing license kerfuffle made migration an easy choice.

So far all the basic functionalities are there in Proxmox:
- snapshots
- ability to format new storage and thin provision
- move guest machines to new storage
- guest agent allows an easy to use command line
- resource usage by guests is the same or slightly less

Nice features are templates you can download and use for most mainstream Linus distro's.

There are curious features:
- you can only enable or make changes to the guest agent when the guest is shut down
- features have changed substantially with different versions so hunting for answers on the web can be confusing





Tags: [virtualization] [linux] 
