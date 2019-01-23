Vagrant.configure("2") do |config|
    config.vm.box = "debian/jessie64"

    config.vm.define 'maquina3' do |node|
        node.vm.hostname = 'maquina3.local'
        config.vm.network "forwarded_port", guest: 80, host: 8000
        config.vm.network "public_network", ip: "10.20.213.51"
        config.vm.network "public_network", bridge: "en1: Wi-Fi (AirPort)"
        node.vm.provision "ansible" do |ansible|
            ansible.playbook = "main.yml"
        end
    end
end