# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|  
  config.vm.define "dev" do |d|
    d.vm.synced_folder ".", "/vagrant", disabled: true
    d.vm.box = "drajen/freenas9"
    d.vm.hostname = "dev" 
    d.vm.network "public_network", bridge: "eno4",   ip: "192.168.57.81" 
#    d.vm.network "public_network", bridge: "eno4",   ip: "192.168.57.80", auto_config: "false", netmask: "255.255.255.0" , gateway: "192.168.57.1"
#    default_router = "192.168.57.1"
#    d.vm.provision :shell, inline: "ip route delete default 2>&1 >/dev/null || true; ip route add default via #{default_router}"
    d.vm.provider "virtualbox" do |v|
      v.memory = 2048
    end
  end
end
