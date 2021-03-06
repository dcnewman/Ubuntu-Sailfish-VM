This repository provides a shell script and sources for building an
arv-gcc 4.6.3 toolchain on the Desktop Ubuntu 12.04.5 operating system.
Links are also provided to a pre-built, 64bit Ubuntu 12.04.5 Virtual Machine
(VM) with directions on using them with the free
[VirtualBox](https://www.virtualbox.org/) and
[Vagrant VM manger](https://www.vagrantup.com/) software.  This pre-built
VM has a working avr-gcc 4.6.3 tool chain installed to `/usr`.  Furthermore,
the tarballs used to build the tool chain as well as the expanded sources
are also stored in the VMs:

* Tool chain sources: `/home/vagrant/avr-gcc-toolchain/`
* Tarballs: `/home/vagrant/avr-gcc-toolchain/incoming/`
* Download and build script: `/home/vagrant/avr-gcc-toolchan/build-avr-gcc.sh`

Keep in mind that the tool chain is already built and installed in
`/usr`.  You do not need to build it again.  The sources and build
directories are provided for reference.

As github has a maximum file size of 100 MB, the pre-built VM is
stored at Dropbox

* [64bit Ubuntu 12.04.5](https://www.dropbox.com/s/esnd0m2fnwlr2rk/ubuntu-64-12.04.5.box?dl=0): 1.36 GB; MD5 checksum 79974a05065d6b546ba2b7cef1ce805e

The virtual machine is a [VirtualBox](https://www.virtualbox.org/) VM
packaged for use with the [Vagrant VM manger](https://www.vagrantup.com/).
You will need to download and install both VirtualBox and Vagrant in
order to use the package.

Once VirtualBox and Vagrant are installed and you have downloaded
`package.box`, issue these commands for a 64 bit VM

    vagrant box add ubuntu-64-12.04.5 ubuntu-64-12.04.5.box
    vagrant init ubuntu-64-12.04.5
    vagrant up

You can then log in to the running VM with the command

    vagrant ssh

To shut down the box, use the command

    vagrant halt

After you have issued the `vagrant up` command, you will see the VM
in the VirtualBox Manager window.  It will have a name similar to
`vagrant_default_someuniquenumber`.  You can actually power it off
and then restart it with its windowing system running from VirtualBox.
(Vagrant will run it headless by default.)  To power off, right click
in VirtualBox on the VM and select "Power Off" under "Close".

The default login account is `vagrant` with password `vagrant`.  The root
account also has the password `vagrant`.  The default Vagrant ssh keys are
installed for the `vagrant` account.


