# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

    config.vm.box = "chef/fedora-20"
    config.vm.box_url = "https://vagrantcloud.com/chef/fedora-20/version/1/provider/virtualbox.box"

    # Use private subnet for local access
    config.vm.network :private_network, ip: "169.254.10.10"
    config.vm.network "forwarded_port", guest: 8080, host: 8080

    # Use rsync for syncing - avoids using slow NFS share
    config.vm.synced_folder ".", "/vagrant", type: "rsync", rsync__args: "-rLptvzDPO"

    # Provision with ansible
    config.vm.provision "ansible" do |ansible|
        ansible.playbook = "provision/vagrant.yml"
    end
end
