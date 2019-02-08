# packer-ubuntu

-   [automate-vsphere-template-builds-packer](https://www.thehumblelab.com/automate-vsphere-template-builds-packer/)
-   [Get host setup](https://nickcharlton.net/posts/using-packer-esxi-6.html)
-   [Good example of packer file for vmware](https://github.com/chef/bento/blob/master/ubuntu/ubuntu-18.10-amd64.json)

Install [ovftool](https://www.vmware.com/support/developer/ovf/) and get it setup by running something like `ovftool --acceptAllEulas --name=mytemplate --datastore=datastore1 --diskMode=thin --network=VM\ Network  vi://root:password@<ip>/datacenter`
this will create $HOME/.ovftool.ssldb which is needed for every esxi host you will be converting images from. [Look here for details](https://github.com/hashicorp/packer/issues/4289).
