Configuration Files for devstack deployment
=============

localrc is deprecated but that's what we're using right now.  
Variables can be found in stackrc file.

More information:

http://devstack.org/localrc.html

# Install devstack on a VM inside your OS

So you want to install devstack on a VM in your machine?  These instructions are the basics for getting up and running on a Mac with VirtualBox and Vagrant.

N.B. Every Mac developer should install Homebrew (http://brew.sh/).  This is similar to aptitude on Ubuntu and is the package manager you should use to install most things (except vagrant ironically).

1. http://www.vagrantup.com/ - this has instructions for installing Vagrant on Mac
1. Clone https://github.com/kili/devstack-conf/tree/master to a folder (I have a folder ~/dev/ for stuff like this)
1. From within that folder, type `vagrant up`
1. It will probably prompt you to download a new box as defined by the VagrantFile you just downloaded. In this case it's precise64
1. You will also want to install the latest and greatest VirtualBox as well or you can also use VMWare
1. Type `vagrant ssh` to ssh into the new machine you just created
1. Now install devstack from within the Ubuntu box (http://devstack.org/guides/single-vm.html) and ignore the localrc modifications in those instructions
1. Use the localrc file from the devstack-conf repository in step 2 above
1. Type `./stack.sh` to launch the stack
1. http://192.168.33.10 should be the address at which the Horizon dashboard is available from your web browser.
