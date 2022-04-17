
Vagrant.configure("2") do |config|
 
  config.vm.box = "ubuntu/trusty64"
  
    config.vm.network "forwarded_port", guest: 80, host: 8080, host_ip: "127.0.0.1"
  
    config.vm.provider "virtualbox" do |vb|
      vb.memory = "4000"
    end

  config.vm.provision "file", source: "./TicTacToe", destination: "/tmp/TicTacToe"
  
  config.vm.provision "shell", inline: <<-SHELL
  sudo apt-get update
  sudo apt-get -y upgrade
  sudo apt-get install -y nginx
  sudo apt-get install -y curl
  sudo cp -r /tmp/TicTacToe/. /usr/share/nginx/html
  SHELL

end
