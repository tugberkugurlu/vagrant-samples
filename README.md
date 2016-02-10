## Run

You need:

 - [Vagrant](https://www.vagrantup.com/) (installation guide: https://www.vagrantup.com/docs/installation/)
 - [VirtualBox](https://www.virtualbox.org/)

First, get the box (the one that has been prepared [here](http://www.hurryupandwait.io/blog/in-search-of-a-light-weight-windows-vagrant-box)):

```
vagrant box add mwrock/Windows2012R2
```

When you run the below commands, it will: 

 - get the Windows Server VM up and running on VirtualBox
 - runs the `Get-Process` PowerShell command on the VM
 - destroys the VM afterwards (doesn't remove the box, you may instead want to [HALT](https://www.vagrantup.com/docs/cli/halt.html))

```
vagrant up
vagrant powershell --command "get-process"
vagrant destroy
```

## Resources

 - http://www.hurryupandwait.io/blog/in-search-of-a-light-weight-windows-vagrant-box
 - https://www.vagrantup.com/docs/virtualbox/configuration.html
 - http://stackoverflow.com/questions/17687648/how-can-i-change-where-vagrant-looks-for-its-virtual-hard-drive
 - https://www.vagrantup.com/docs/boxes/base.html