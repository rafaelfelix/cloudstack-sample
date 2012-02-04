Vagrant::Config.run do |config|

  # Cloud manager
  config.vm.define :cm_server do |cm_config|
    cm_config.vm.box = "centos6-minimal"
    cm_config.vm.forward_port("web", 80, 8001)
    cm_config.vm.provision :puppet do |puppet|
      puppet.module_path    = "modules"
      #puppet.options        = "--verbose --debug"
      puppet.manifests_path = "manifests"
      puppet.manifest_file  = "cm.pp"
    end
  end

  # Xen host 01 
  config.vm.define :h1_server do |h1_config|
    h1_config.vm.box = "centos6-minimal"
    #h1_config.vm.forward_port("web", 8080, 8001)
    h1_config.vm.provision :puppet do |puppet|
      puppet.module_path    = "modules"
      #puppet.options        = "--verbose --debug"
      puppet.manifests_path = "manifests"
      puppet.manifest_file  = "xen-host.pp"
    end
  end

  # Xen host 02
  config.vm.define :h2_server do |h2_config|
    h2_config.vm.box = "centos6-minimal"
    #h2_config.vm.forward_port("web", 8080, 8001)
    h2_config.vm.provision :puppet do |puppet|
      puppet.module_path    = "modules"
      #puppet.options        = "--verbose --debug"
      puppet.manifests_path = "manifests"
      puppet.manifest_file  = "xen-host.pp"
    end
  end
	
end
