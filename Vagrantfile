# -*- mode: ruby -*-
# vi: set ft=ruby :
#VAGRANTFILE_API_VERSION = "2"

Vagrant.configure("2") do |config|
  config.vm.box      = "centos/7"
  
#  if Vagrant.has_plugin?("vagrant-hostmanager")
#     config.hostmanager.enabled = true
#     config.hostmanager.manage_host = true
#     config.hostmanager.ignore_private_ip = false
#     config.hostmanager.include_offline = true
#  end
   

#  config.vm.provision "ansible" do |ansible|
#    ansible.verbose = "v"
#    ansible.playbook = "site.yml"
#    ansible.become = true
#    ansible.compatibility_mode = "2.0"
    #ansible.raw_arguments = "-v"
    #ansible.sudo = true
    #ansible.raw_arguments  = "--vault-password-file=vars/vault_pass.txt"
#  end


    config.vm.define "dev1" do |dev1|
      dev1.vm.hostname = "dev1"
      dev1.vm.network :public_network, :ip => "add_ip", :mac => "add_me", :bridge => "en8: USB 10/100/1000 LAN", :use_dhcp_assigned_default_route => true
  end

    config.vm.define "dev2" do |dev2|
      dev2.vm.hostname = "dev2"
      dev2.vm.network :public_network, :ip => "add_ip", :mac => "add_me", :bridge => "en8: USB 10/100/1000 LAN", :use_dhcp_assigned_default_route => true
  end


    config.vm.provider "virtualbox" do |v|
      v.memory = 512
      #v.memory = 1024
      v.cpus = 1
  end
end
