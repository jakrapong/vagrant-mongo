# vagrant-mongo
Ubuntu MongoDB 3.2.1 server implemented with Vagrant


Requirements
------------
* VirtualBox <http://www.virtualbox.com>
* Vagrant <http://www.vagrantup.com>
* Git <http://git-scm.com/>
* Ansible <http://docs.ansible.com/ansible/intro_installation.html>

Usage
-----

### Startup
	$ git clone https://github.com/jakrapong/vagrant-mongo.git
	$ cd vagrant-lamp
	$ vagrant up

That is pretty simple.

### Connecting

#### MongoDB
MongoDB server is available at port localhost:27017, no password required


Technical Details
-----------------
* Debian Wheezybox
* MongoDB 3.2.1

And like any other vagrant file you have SSH access with

	$ vagrant ssh