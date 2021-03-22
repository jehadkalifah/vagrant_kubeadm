# vagrant plugin install vagrant-disksize
BOX_IMAGE = "ubuntu/bionic64"

Vagrant.configure("2") do |config|
  config.vm.define "master01" do |subconfig|
    subconfig.vm.box = BOX_IMAGE
	#subconfig.vm.boot_timeout = 5
	subconfig.vm.box_check_update = false
    subconfig.vm.hostname = "master01"
    subconfig.disksize.size = '100GB'  
    subconfig.vm.network "public_network", ip: "192.168.0.30"
    subconfig.vm.provider "virtualbox" do |v|
       v.memory = 3072
       v.cpus = 4
    end
  end 
  config.vm.define "worker01" do |subconfig|
    subconfig.vm.box = BOX_IMAGE
	#subconfig.vm.boot_timeout = 5
	subconfig.vm.box_check_update = false
    subconfig.vm.hostname = "worker01"
    subconfig.disksize.size = '100GB'	  
    subconfig.vm.network "public_network", ip: "192.168.0.40"
    subconfig.vm.provider "virtualbox" do |vb|
       vb.memory = 3072
       vb.cpus = 4
    end
  end 
    config.vm.define "worker02" do |subconfig|
    subconfig.vm.box = BOX_IMAGE
	#subconfig.vm.boot_timeout = 5
	subconfig.vm.box_check_update = false
    subconfig.vm.hostname = "worker02"
    subconfig.disksize.size = '100GB'	    
    subconfig.vm.network "public_network", ip: "192.168.0.50"
    subconfig.vm.provider "virtualbox" do |vb|
       vb.memory = 3072
       vb.cpus = 4
    end
  end 

end
