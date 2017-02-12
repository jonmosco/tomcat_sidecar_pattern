# -*- mode: ruby -*-
# vi: set ft=ruby

Vagrant.configure('2') do |config|

  config.vm.provision "shell", path: "script.sh"

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yml"
  end

  # webserver
  config.vm.define 'docker01' do |docker01|
    docker01.vm.box = "centos/7"
    docker01.vm.hostname = 'docker02'
    docker01.vm.network :forwarded_port, guest: 8080, host: 8888
  end

end
