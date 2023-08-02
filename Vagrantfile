SSH_KEY = "/home/ubuntu/.ssh/id_rsa.pub"
hostname = "officemag01"


Vagrant.configure("2") do |config|
  config.vm.define hostname do |node|
    node.vm.box = "bento/ubuntu-18.04"
    node.vm.box_check_update = false
    node.vm.hostname = hostname
    node.vm.provision "shell", inline: "echo '#{File.read(SSH_KEY)}' >> /home/vagrant/.ssh/autorized_keys"
    node.vm.network "public_network", ip: "192.168.1.150", hostname: true
  
    config.vm.provider "virtualbox" do |v|
      v.memory = 2048
      v.cpus = 2
      v.name = hostname
	  end	
    config.vm.provision "ansible" do |ansible| 
      ansible.playbook = "playbook.yml"
      ansible.inventory_path = "./inventory/"
      ansible.compatibility_mode = "2.0"
      SSH_KEY = "/home/ubuntu/vagrant_keys/id_rsa.pub"
    end
  end
end

