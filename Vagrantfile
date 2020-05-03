# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.vm.define "metropolitana" do |metropolitana|
  	metropolitana.vm.box = "generic/ubuntu1804"
  	metropolitana.vm.box_check_update = false
  	metropolitana.vm.network "private_network", ip: "192.168.33.2"
  	metropolitana.vm.hostname = "metropolitana"
  	config.ssh.insert_key = false
  	#metropolitana.vm.provision :shell, :inline => "sudo sed -i 's/PasswordAuthentication no/PasswordAuthentication yes/g' /etc/ssh/sshd_config; sudo systemctl restart sshd;", run: "always"
  	config.vm.provider "virtualbox" do |v|
		v.memory = 1024
		#v.cpus = 1
	 end
  end
  config.vm.define "ansiblemetropolitana" do |ansiblemetropolitana|
  	ansiblemetropolitana.vm.box = "generic/ubuntu1804"
  	#metropolitana.vm.box_check_update = false
  	ansiblemetropolitana.vm.network "private_network", ip: "192.168.33.3"
  	ansiblemetropolitana.vm.hostname = "ansiblemetropolitana"
  	ansiblemetropolitana.vm.synced_folder "Documents", "/home/vagrant/Documents"
  	config.ssh.insert_key = false
  	#ansiblemetropolitana.vm.provision :shell, :inline => "sudo sed -i 's/PasswordAuthentication no/PasswordAuthentication yes/g' /etc/ssh/sshd_config; sudo systemctl restart sshd;", run: "always"
  	ansiblemetropolitana.vm.provider "virtualbox" do |v1|
		v1.memory = 1024
		#v1.cpus = 1
	 end
  end

	  
end
