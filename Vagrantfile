Vagrant.configure("2") do |config|
 config.vm.box = "hashicorp/bionic64"

 (1..2).each do |i|
   config.vm.define "web#{i}" do |web|
     #we will setup our IPs for both web1 and web2 
     #IPs will look like this:
     #WEB1: 192.168.50.11
     #WEB2: 192.168.50.12
     web.vm.network "private_network", ip: "192.168.50.#{i+10}" 
     #install webserver
     web.vm.provision "shell", inline: "apt-get update ; apt-get install -y nginx"
  end
 end
end
