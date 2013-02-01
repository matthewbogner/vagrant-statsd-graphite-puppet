Vagrant::Config.run do |config|

  config.vm.box = "statsbox"
  config.vm.box_url = "https://github.com/downloads/divio/vagrant-boxes/vagrant-ubuntu-11.04-server-amd64-v1.box"

  # Assign this VM to a host only network IP, allowing you to access it
  # via the IP.
  config.vm.network :hostonly, "10.0.0.34"

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
