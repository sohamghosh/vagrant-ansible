# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "centos"

  config.vm.network :private_network, ip: "192.168.33.61"

  config.vm.provision "ansible" do |ansible|
      ansible.playbook = "provisioning/playbook.yml"
      ansible.inventory_path = "hosts"
      ansible.verbose = "v"
  end

end
