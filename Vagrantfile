Vagrant.require_version ">= 1.7.0"

Vagrant.configure("2") do |config|
  
  config.vm.define "bs" do |s|
    
    s.vm.box = "ubuntu/xenial64"
    s.vm.network "private_network", ip: "192.168.10.101"
     
    config.vm.provision "ansible" do |ansible|
      ansible.verbose = "v"
      ansible.playbook = "vagrant-provisioning.yml"
      ansible.extra_vars = { ansible_python_interpreter: "/usr/bin/python3" }
    end
     
    s.vm.provider :virtualbox do |vb|
      vb.name = "Build Server"
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
