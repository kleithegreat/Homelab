Vagrant.configure("2") do |config|
  config.vm.box = "generic/ubuntu2204"
  config.vm.hostname = "homeserver"

  config.vm.provider :libvirt do |libvirt|
    libvirt.memory = 16384
    libvirt.cpus = 2
    libvirt.driver = "kvm"
  end

  config.vm.network :private_network, ip: "192.168.121.10"
  config.vm.synced_folder ".", "/vagrant", type: "rsync"
end