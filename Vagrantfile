Vagrant::Config.run do |config|

  config.vm.box = "ubuntu12"
  config.vm.box_url = "http://files.vagrantup.com/precise64.box"

  # Assign this VM to a host only network IP, allowing you to access it
  # via the IP.
  config.vm.network :hostonly, "10.0.10.34"

  # Configure DNS according with the new version of vagrant
  config.vm.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]

  # Forward a port from the guest to the host, which allows for outside
  # computers to access the VM, whereas host only networking does not.
  config.vm.forward_port 80, 8034
  config.vm.forward_port 2003, 2003
  config.vm.forward_port 8125, 8125, { :protocol => 'udp' }

  # Share an additional folder to the guest VM. The first argument is
  # an identifier, the second is the path on the guest to mount the
  # folder, and the third is the path on the host to the actual folder.
  # config.vm.share_folder "v-data", "/vagrant_data", "../data"

  config.vm.provision :puppet do |puppet|
    puppet.manifests_path = "manifests"
    puppet.manifest_file  = "base.pp"
  end
end
