# -*- mode: ruby; -*-
Vagrant.configure("2") do |config|
  config.vm.box = "krlex/freebsd-12.1.2-cbsd"
  config.vm.hostname = "vagrant"
  config.vm.network "private_network", ip: "192.168.33.20"
  config.vm.provision :ansible do |ansible|
    ansible.playbook = "provision/site.yml"
    ansible.host_key_checking = false
    ansible.raw_arguments = ["-e", "ansible_python_interpreter='/usr/bin/env python3.7'"]
    ansible.groups = {
      "vagrant" => ["default"],
    }

  end
end
