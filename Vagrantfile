Vagrant.configure("2") do |config|
  config.vm.define :master do |master|
    master.vm.box = "bento/ubuntu-20.04"
    master.vm.network :private_network, ip: "192.168.50.10"
    master.vm.hostname = "master"
	config.vm.provision "shell" do |s|
	s.inline = "mkdir /etc/gcrypt;"\
			"echo all >> /etc/gcrypt/hwf.deny;"\
			"sudo apt-get update;"\
			"sudo apt install tree;"\
			"sudo apt install git;"\
			"sudo apt install docker -y;"\
			"sudo apt install docker-compose -y;"\
			"sudo apt install default-jre -y;"\
			"sudo apt install python3-pip -y;"\
			"sudo apt-get update;"\
			end
  end

  config.vm.define :node1 do |node1|
    node1.vm.box = "bento/ubuntu-20.04"
    node1.vm.network :private_network, ip: "192.168.50.21"
    node1.vm.hostname = "node1"
  end
  
    config.vm.define :node2 do |node2|
    node2.vm.box = "bento/ubuntu-20.04"
    node2.vm.network :private_network, ip: "192.168.50.22"
    node2.vm.hostname = "node2"
  end
  
    config.vm.define :node3 do |node3|
    node3.vm.box = "bento/ubuntu-20.04"
    node3.vm.network :private_network, ip: "192.168.50.23"
    node3.vm.hostname = "node3"
  end
  
    config.vm.define :node4 do |node4|
    node4.vm.box = "bento/ubuntu-20.04"
    node4.vm.network :private_network, ip: "192.168.50.24"
    node4.vm.hostname = "node4"
  end
end
