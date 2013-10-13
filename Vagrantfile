# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # Every Vagrant virtual environment requires a box to build from. Here
  # we are using 64-bit Ubuntu 12.04. It will be fetched from the remote
  # URL if not already installed.
  config.vm.box = "precise64"
  config.vm.box_url = "http://files.vagrantup.com/precise64.box"

  # If true, then any SSH connections made will enable agent forwarding.
  # Default value: false
  # config.ssh.forward_agent = true

  # Provider-specific configuration so you can fine-tune various
  # backing providers for Vagrant. These expose provider-specific options.
  # For VirtualBox:
  config.vm.provider :virtualbox do |vb|
    # Don't boot with headless mode
    # vb.gui = true
    # Use VBoxManage to customize the VM. For example to change memory:
    vb.customize ["modifyvm", :id, "--memory", "512"]
  end

  # Create four box definitions on different IPs on a private network.
  config.vm.define "mirror-a" do |subconfig|
    subconfig.vm.network :private_network, ip: "192.168.99.10"
  end
  config.vm.define "mirror-b" do |subconfig|
    subconfig.vm.network :private_network, ip: "192.168.99.11"
  end
  config.vm.define "mirror-c" do |subconfig|
    subconfig.vm.network :private_network, ip: "192.168.99.12"
  end
  config.vm.define "mirror-d" do |subconfig|
    subconfig.vm.network :private_network, ip: "192.168.99.13"
  end
end
