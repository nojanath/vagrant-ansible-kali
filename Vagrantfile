# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "kalilinux/rolling"

  config.vm.box_check_update = true
  # config.vm.network "forwarded_port", guest: 80, host: 8080
  # config.vm.network "forwarded_port", guest: 80, host: 8080, host_ip: "127.0.0.1"
  # config.vm.network "private_network", ip: "192.168.33.10"
  config.vm.network "public_network", bridge: [
      "en0: Wi-Fi (AirPort)"
  ]
  # config.vm.synced_folder "../data", "/vagrant_data"

  config.vm.provider "vmware_desktop" do |v|
    v.gui = true
    v.allowlist_verified = true
    v.vmx["memsize"] = "4096"
    v.vmx["numvcpus"] = "4"
  end

  config.vm.provision "ansible_local" do |ansible|
    ansible.install_mode = :default
    ansible.playbook = "provision/playbook.yml"
  end
end
