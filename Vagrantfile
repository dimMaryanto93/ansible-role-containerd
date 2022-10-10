Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"

  config.vm.define "master" do |ctlpanel|
    ctlpanel.vm.hostname = "vm-k8s-master.dimas-maryanto.com"
    ctlpanel.vm.network "private_network", ip: "192.168.56.10", name: "vboxnet0"
    ctlpanel.vm.network "forwarded_port", id: "ssh", host: 2210, guest: 22
    ctlpanel.vm.provider :virtualbox do |vm|
      vm.memory = 4096
      vm.cpus = 2
      vm.gui = false
    end
  end

end
