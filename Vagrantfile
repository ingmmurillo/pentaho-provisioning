# -*- mode: ruby -*-
# vi: set ft=ruby :

ANSIBLE_GROUPS = {"vagrant" => ["default"]}

Vagrant.configure(2) do |config|
  #Vagrant Box https://atlas.hashicorp.com/boxes/search
  config.vm.box = "centos/7"
  config.vm.network :forwarded_port, guest: 8080, host: 8888
  config.cache.scope = :box if Vagrant.has_plugin?("vagrant-cachier")

  #Sync Folder
  config.vm.synced_folder "shared/", "/home/vagrant/", create: false,
    owner: "vagrant", group: "vagrant"

  #Code to provision the box
  config.vm.provision "ansible" do |ansible|
    ansible.groups = ANSIBLE_GROUPS
    ansible.playbook = "playbook.yml"
  end

end
