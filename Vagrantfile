# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = 'ubuntu/trust64'

  virtual_machines = {
    'tasukuforce' => '10.11.12.13'
  }

  virtual_machines.each do |hostname, ip|
    config.define hostname do |host|
      host.vm.network :private_network, ip: ip
      host.vm.hostname = "#{hostname}.wordpress.dev"
    end
  end
end