# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "ubuntu/trusty64"
  # http://stackoverflow.com/questions/5984217/vagrants-port-forwarding-not-working
  # run server with “python manage.py runserver 0.0.0.0:8000” 
  #to avoid the 127.0.0.1 loopback issue
  config.vm.network "forwarded_port", guest: 8000, host: 8000
  config.vm.provision :shell, path: "provision/django.sh"
end
