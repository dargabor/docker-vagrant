IMAGE_NAME = "ubuntu/bionic64"

Vagrant.configure("2") do |config|

    config.vm.box = IMAGE_NAME
    config.vm.network "private_network", ip: "192.168.50.20"
    config.vm.provision "ansible_local" do |ansible|
        ansible.playbook = "provision/docker-playbook.yml"
        ansible.compatibility_mode = "2.0"
        ansible.extra_vars = {
            ansible_python_interpreter:"/usr/bin/python3",
        }
    end
   
end
