$ vagrant init hashicorp/precise64

Add following lines to Vagrantfile. 
config.vm.network "private_network", ip: "192.168.33.10"

And maybe following too. 
config.vm.provider "virtualbox" do |v|
    v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
    v.customize ["modifyvm", :id, "--natdnsproxy1", "on"]
end


$ vagrant up
