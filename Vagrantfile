
Vagrant.configure(2) do |config|

  config.vm.box = "ubuntu/trusty64"

  config.vm.synced_folder Dir.pwd, "/app/"

  config.vm.define :McboTechMeetUp do |conf|
    conf.vm.network :forwarded_port, guest: 8585, host: 8585, ngrok_proto: "http+https"
  end

  config.vm.provision :ansible do |ansible|
      ansible.playbook = "playbook.yml"
      ansible.verbose = "vvvv"
  end


end
