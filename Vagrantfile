# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  	config.vm.define "mongo_db" do |mongo_db|
		mongo_db.vm.box = "server4001/node-mongodb-centos"
		mongo_db.vm.network "forwarded_port", guest: 1521, host: 1521, host_ip: "127.0.0.1"
		# oracle_db.vm.network "private_network", type: "dhcp"
		mongo_db.vm.network "private_network", ip: "25.25.25.3"
		mongo_db.vm.synced_folder ".", "/vagrant", disabled: true
		# mongo_db.vm.synced_folder "oracle_share", "/home/vagrant"
		# mongo_db.vm.provision "shell", path: "vagrant_bootstrap_oracle.sh"
  	end
end
