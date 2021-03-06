# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  # m38 Base Vagrant image
  config.vm.box = 'ubuntu/trusty64'

  # Check for box updates
  config.vm.box_check_update = true

  # Configure host-only network
  config.vm.network 'private_network', ip: '192.168.70.4'
  config.vm.network "forwarded_port", guest: 80, host: 8880
  config.vm.network "forwarded_port", guest: 8080, host: 8887

  config.ssh.forward_agent = true
  # Share folder, disabled sync by default due to issues on windows with SMB
  # sharing. You can enable sync by setting the VAGRANT_SYNC_ENABLED env var
  # to true.
  sync_disabled = true
  if ENV['VAGRANT_SYNC_ENABLED']
    sync_disabled = !ENV['VAGRANT_SYNC_ENABLED']
  end

  config.vm.synced_folder './', '/home/vagrant/app', disabled: sync_disabled

  # Configure the virtual machine to use 2GB of RAM
  config.vm.provider :virtualbox do |vb|
    vb.name = "todomvc"
    vb.customize [
                     'modifyvm', :id,
                     '--memory', '1024',
                     '--cpus', '1'
                 ]
  end

  config.vm.provision "shell", path: "provision/system.sh"
end
