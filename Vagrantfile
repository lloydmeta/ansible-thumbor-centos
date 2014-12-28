# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.network :forwarded_port, guest: 22, host: 2299
  config.vm.network :forwarded_port, guest: 80, host: 8080

  config.vm.define "centOS_7_thumbor" do |instance|

    # Every Vagrant virtual environment requires a box to build off of.
    instance.vm.box = 'hfm4/centos7'

    # View the documentation for the provider you're using for more
    # information on available options.
    config.vm.provision "ansible" do |ansible|
      ansible.playbook = "site.yml"
      ansible.verbose = 'vv'
      ansible.sudo = true
    end
  end
end
