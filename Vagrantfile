Vagrant.configure("2") do |config|
  (1..3).each do |i|
    config.vm.define "server#{i}" do |node|
      node.vm.box = "ubuntu/bionic64"
      node.vm.hostname = "server#{i}"
      node.vm.network "private_network", ip: "192.168.33.1#{i}"  # IPs estáticas
      node.vm.provider "virtualbox" do |vb|
        vb.memory = "256"
        vb.cpus = 1
      end
    end
  end
end


