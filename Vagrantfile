Vagrant.configure("1") do |config|
    config.vm.box = "ubuntu/bionic64"
    config.vm.network "forwarded_port", guest: 8080, host: 8080
    config.vm.network "forwarded_port", guest: 8081, host: 8081
    config.vm.network "forwarded_port", guest: 8082, host: 8082
    config.vm.provision "shell", path: "./provisionning/script_ansible.sh"
   #config.vm.synced_folder ".", "/vagrant"
    config.vm.provision "ansible_local" do |ansible|
        ansible.playbook = "provisionning/playbook.yml"
    end
end
