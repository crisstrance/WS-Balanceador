Vagrant.configure("2") do |config|
	### balanceador
	 config.vm.define "balanceador" do |balanceador|
		 balanceador.vm.box = "hashicorp/precise64"
		 balanceador.vm.hostname = "balanceador"
		 balanceador.vm.network "private_network", ip:"192.168.18.8"
		 balanceador.vm.provider "virtualbox" do |vb|
			 vb.memory = 512
			 vb.cpus = 2
		 end
		 balanceador.vm.provision "shell", inline: "sudo service apache2 restart", run: "always"
		 balanceador.vm.provision "shell", inline: "sudo apt-get update && apt-get -y upgrade", run: "always"
	 end
###w1
	 config.vm.define "w1" do |w1|
		 w1.vm.box = "hashicorp/precise64"
		 w1.vm.hostname = "w1"
		 w1.vm.network "private_network", ip:"192.168.18.9"
		 w1.vm.provider "virtualbox" do |vb|
			 vb.memory = 512
			 vb.cpus = 2
		 end
		 w1.vm.provision "shell", inline: "sudo apt-get update && apt-get -y upgrade", run: "always"
		 #w1.vm.synced_folder "www/" , "/var/www"
	 end
###w2
	 config.vm.define "w2" do |w2|
		 w2.vm.box = "hashicorp/precise64"
		 w2.vm.hostname = "w2"
		 w2.vm.network "private_network", ip:"192.168.18.10"
		 w2.vm.provider "virtualbox" do |vb|
			 vb.memory = 512
			 vb.cpus = 2
		 end
		 w2.vm.provision "shell", inline: "sudo apt-get update && apt-get -y upgrade", run: "always"
		 #w2.vm.synced_folder "www/" , "/var/www"
	 end
end