Cannot cut and paste into ESXI virtual machines.  Aieee!  Try typing a 100 character command!  Certainly not an issue that only I am having and judging by the questions [here](https://www.google.com/search?q=vmware+esxi+cut+and+paste) this has been an issue for years since VMWare changed it from allowed by default to disabled due to security reasons.

I followed the usual recommendations and added two parameters to the virtual machine configuration

    Name: isolation.tools.copy.disable, Value: false
    Name: isolation.tools.paste.disable, Value: false
    
Then I shut down the VM, shut down the ESXI server and restarted everything. Nada

Then I tried the VSphere thick console, nada

Then I tried the VRMC console, nada

The most frustrating thing is that when using Chrome and right clicking I can see the cut and paste options but they are grayed out.


Oh well, there's always [Putty](https://www.putty.org/)

Tags: [vmware]
