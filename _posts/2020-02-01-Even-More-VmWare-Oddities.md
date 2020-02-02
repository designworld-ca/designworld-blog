#Error message: Unsupported hardware family ‘vmx-16’ error

If you see this or similar with an image you are trying to import just edit the ovf file and change this line
     <vssd:VirtualSystemType>vmx-16
     to
     <vssd:VirtualSystemType>vmx-10
  
  
  Thanks to [CTOBob](https://ctobob.com/2017/10/02/unsupported-hardware-family-vmx-12-error-vmware-vsphere-esxi-6-6-5/)
     Tags:[vmware]
