# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure('2') do |config|
  config.vm.box      = 'bento/ubuntu-16.04'
  config.vm.hostname = 'redmine'

  config.vm.network :forwarded_port, host: 3000, guest: 3000
  # config.vm.provision :shell, path: 'bootstrap.sh', keep_color: true

  provider = 'vmware_fusion'
  config.vm.provider provider do |v|
    v.memory = 2048
    v.cpus = 2
  end
end
