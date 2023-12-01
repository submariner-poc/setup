Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "8192"
    vb.cpus = 4
    vb.name = "east-cluster"
    config.vm.network "private_network", ip: "192.168.23.10"
  end
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "./ansible/main.yml"      
  end

end