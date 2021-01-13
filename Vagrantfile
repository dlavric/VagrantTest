# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure("2") do |config|
 config.vm.box = "hashicorp/bionic64"

 (1..2).each do |i|
   config.vm.define "web#{i}" do |web|
     #install webserver
     web.vm.provision "shell", inline: "apt-get update ; apt-get install -y nginx"
   end
 end
end
