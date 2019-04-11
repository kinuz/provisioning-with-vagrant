Vagrant.require_version ">= 1.7.0"

Vagrant.configure("2") do |config|
  
  config.vm.define "s1" do |s|
    
    s.vm.box = "my.box"
    s.vm.hostname = "s1"
    s.vm.network "private_network", ip: "192.168.10.101"
     
    s.vm.provider :virtualbox do |vb|
      vb.name = "Server 1"
      vb.customize ["modifyvm", :id, "--memory", 1024]
      vb.customize ["modifyvm", :id, "--cpus", "1"]
      vb.customize ["modifyvm", :id, "--ioapic", "on"]
      vb.customize ["modifyvm", :id, "--nictype1", "virtio" ]
      vb.customize ["modifyvm", :id, "--nictype2", "virtio" ]
      vb.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      vb.customize ["modifyvm", :id, "--natdnsproxy1", "on"]
    end
  end

  config.vm.define "s2" do |s|
      
    s.vm.box = "my.box"
    s.vm.hostname = "s2"
    s.vm.network "private_network", ip: "192.168.10.102"
     
    s.vm.provider :virtualbox do |vb|
      vb.name = "Server 2"
      vb.customize ["modifyvm", :id, "--memory", 1024]
      vb.customize ["modifyvm", :id, "--cpus", "1"]
      vb.customize ["modifyvm", :id, "--ioapic", "on"]
      vb.customize ["modifyvm", :id, "--nictype1", "virtio" ]
      vb.customize ["modifyvm", :id, "--nictype2", "virtio" ]
      vb.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      vb.customize ["modifyvm", :id, "--natdnsproxy1", "on"]
    end
  end

  config.vm.define "s3" do |s|
      
    s.vm.box = "my.box"
    s.vm.hostname = "s3"
    s.vm.network "private_network", ip: "192.168.10.103"
     
    s.vm.provider :virtualbox do |vb|
      vb.name = "Server 3"
      vb.customize ["modifyvm", :id, "--memory", 1024]
      vb.customize ["modifyvm", :id, "--cpus", "1"]
      vb.customize ["modifyvm", :id, "--ioapic", "on"]
      vb.customize ["modifyvm", :id, "--nictype1", "virtio" ]
      vb.customize ["modifyvm", :id, "--nictype2", "virtio" ]
      vb.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      vb.customize ["modifyvm", :id, "--natdnsproxy1", "on"]
    end
  end
  
end
