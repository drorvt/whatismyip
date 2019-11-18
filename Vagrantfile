Vagrant.configure("2") do |config|
    config.vm.box = "elegoev/ubuntu-18.04-docker"
    # Forward port 5000 to localhost so you can access your  app 
    config.vm.network "forwarded_port", guest: 8000, host: 8000, host_ip: "127.0.0.1"
    # Allowing your virtual machine to be provisioned by ANSIBLE
    config.vm.provision "ansible_local" do |ansible|
        ansible.playbook = "Deploy/playbook.yml"
    end
end