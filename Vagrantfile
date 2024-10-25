Vagrant.configure("2") do |config|
    config.vm.provider :vmware_desktop do |vmw|
        vmw.vmx["ethernet0.pcislotnumber"] = "160"
        vmw.gui = false
        vmw.memory = "2000"
        vmw.cpus = 2
    end
    
    config.vm.define "master" do |master|
        master.vm.box = "rwideman/ubuntu2404-arm64"
        master.vm.hostname = "master.local"
    end

    config.vm.define "worker1" do |worker1|
        worker1.vm.box = "rwideman/ubuntu2404-arm64"
        worker1.vm.hostname = "worker1.local"
    end

    config.vm.define "worker2" do |worker2|
        worker2.vm.box = "rwideman/ubuntu2404-arm64"
        worker2.vm.hostname = "worker2.local"
    end
end
