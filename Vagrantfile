# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.network :forwarded_port, guest: 22, host: 2299
  config.vm.network :forwarded_port, guest: 80, host: 8080

  config.vm.define "centOS6.5_thumbor" do |instance|

    # Every Vagrant virtual environment requires a box to build off of.
    instance.vm.box = 'centOS6.5_64_nrel'

    # The url from where the 'config.vm.box' box will be fetched if it
    # doesn't already exist on the user's system.
    instance.vm.box_url = "http://developer.nrel.gov/downloads/vagrant-boxes/CentOS-6.5-x86_64-v20140311.box"

    # View the documentation for the provider you're using for more
    # information on available options.
    config.vm.provision "ansible" do |ansible|
      ansible.playbook = "site.yml"
      ansible.verbose = 'vv'
      ansible.sudo = true
    end
  end
end
