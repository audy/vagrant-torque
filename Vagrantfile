# -*- mode: ruby -*-
# vi: set ft=ruby :


VAGRANTFILE_API_VERSION = '2'

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

 config.vm.provider 'virtualbox' do |v|
      v.customize ['modifyvm', :id, '--memory', '512']
      v.customize ['modifyvm', :id, '--cpus', '12']
      v.customize ['modifyvm', :id, '--ioapic', 'on']
  end

  config.vm.define :master do |master|
    master.vm.box = 'precise32'
    master.vm.box_url = 'http://files.vagrantup.com/precise32.box'
    master.vm.network :private_network, ip: '192.168.1.100'
    master.vm.hostname = 'master'

    master.vm.provision :shell, :path => 'setup.sh'
  end
end
