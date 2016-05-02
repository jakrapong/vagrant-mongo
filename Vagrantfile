# -*- mode: ruby -*-
# vi: set ft=ruby :


Vagrant.configure(2) do |config|

 	config.vm.box = 'debianwheezybox'
	config.vm.box_url = 'https://downloads.sourceforge.net/project/vagrantdebianboxes/debianwheezy.box?r=&ts=1374688209&use_mirror=heanet'

	config.vm.network "forwarded_port", guest: 27017, host: 27017   # mongo

	config.vm.hostname = "MongoRedis"

	config.vm.provider 'virtualbox' do |v|
		v.memory = 2048
	end

	config.vm.provision "shell" do |s|
		s.inline = "echo 'LC_ALL=\"en_GB.utf8\"' >> /etc/default/locale"
	end

	config.vm.provision "ansible" do |ansible|
		ansible.playbook = "ansible/site.yml"
		ansible.sudo = true
		# ansible.verbose = "vvvv"
	end
end
