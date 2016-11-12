# -*- mode: ruby; -*-
Vagrant.configure("2") do |config|
  config.vm.box = "freebsd/FreeBSD-11.0-STABLE"
  config.vm.hostname = "vagrant"
  config.vm.network "private_network", ip: "192.168.33.20"
  config.vm.provision :ansible do |ansible|
    ansible.playbook = "provision/site.yml"
    ansible.host_key_checking = false
    ansible.groups = {
      "vagrant" => ["default"],
    }

  end
end
