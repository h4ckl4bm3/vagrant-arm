Vagrant.configure(2) do |config|

  config.vm.box = "ubuntu/trusty64"
  config.vm.synced_folder "./shared", "/shared"

  config.vm.provider "virtualbox" do |vb|
      vb.memory = "2048"
  end

  config.vm.provision "shell", inline: <<-SHELL
     sudo apt-get update
     sudo apt-get -y install gcc-arm-linux-gnueabi
     sudo apt-get -y install qemu
  SHELL

end
