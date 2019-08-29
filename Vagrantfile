# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure("2") do |config|
    config.vm.box = "bento/ubuntu-14.04"
    # config.ssh.username = 'root'
    # config.ssh.password = 'vagrant'
    # config.ssh.insert_key = 'true'

    # If true, Vagrant will automatically insert a keypair
    # to use for SSH, replacing Vagrant's default insecure key 
    # inside the machine if detected. By default, this is true
    config.ssh.insert_key = false

    # Configures synced folders on the machine, so that folders 
    # on your host machine can be synced to and from the guest machine
    config.vm.synced_folder ".", "/vagrant", disabled: true
    
    # VM Provider
    config.vm.provider :virtualbox do |v|
        v.memory = 256
        v.linked_clone = true
    end

    # # Web server
    # config.vm.define "mattermost" do |mattermost|
    #     mattermost.vm.hostname = "mattermost"
    #     # static ip address
    #     mattermost.vm.network :private_network, ip: "192.168.60.4"
    # end
    


    # Iptv server
    config.vm.define "iptv" do |iptv|
        iptv.vm.hostname = "iptv"
        # static ip address
        iptv.vm.network :private_network, ip: "192.168.60.6"
    end 

    # web server
    config.vm.define "web-server" do |web|
        web.vm.hostname = "web"
        # static ip address
        web.vm.network :private_network, ip: "192.168.60.7"
    end
end
