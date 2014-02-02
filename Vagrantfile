# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

$script = <<EOF
/bin/bash /vagrant/provision/bootstrap.sh
cd /home/vagrant
sudo -u vagrant virtualenv --system-site-packages ./env
sudo -u vagrant ./env/bin/pip install skype4py
sudo -u vagrant mkdir /home/vagrant/.Skype
sudo -u vagrant cp /vagrant/provision/shared.xml /home/vagrant/.Skype/shared.xml
cp /vagrant/provision/*.conf /etc/init/
start xvfb
EOF

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "precise32"
  config.vm.box_url = "http://files.vagrantup.com/precise32.box"
  config.vm.network :private_network, ip: "192.168.33.10"
  config.vm.provision "shell", inline: $script
end
