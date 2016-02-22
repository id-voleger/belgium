# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "bento/ubuntu-10.04"
  config.vm.network "private_network", ip: "192.168.33.20"
  config.vm.synced_folder "site/", "/var/www/site", create: true,
    owner: "www-data", group: "www-data"

  config.vm.provider "virtualbox" do |vb|
    vb.cpus = "2"
    vb.memory = "2048"
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "site.yml"
  end

end
