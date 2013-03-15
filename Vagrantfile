require 'vagrant-ansible'

Vagrant::Config.run do |config|
  config.vm.box     = "ubuntu-12.04"
  config.vm.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
  
  config.vm.provision :ansible do |ansible|
    ansible.sudo = true

    #ansible.playbook = "newservers/newservers.yml"
    #ansible.hosts = "newservers"

    ansible.playbook = "bitlbee/main.yml"
    ansible.hosts = "chatservers"
  end
end
