Vagrant.configure("2") do |config|
  config.vm.box = "hashicorp/bionic64"
  config.vm.define:app do |app_config|
    app_config.vm.network "public_network", ip: "192.168.0.77"
    
    app_config.vm.provision "shell", inline: "sudo apt-get update && sudo apt-get install -y nginx"
    app_config.vm.synced_folder "./data", "/var/www/html"
    app_config.vm.provider:virtualbox do |v|
      v.name = "VM Vagrant"
    end
  end
end
