#
# Single box with LAMP stack and bare site via Puppet.
#
box      = 'precise64'
url      = 'http://files.vagrantup.com/precise64.box'
hostname = 'BARE'
domain   = 'BARE.dev'
ip       = '192.168.0.45'
ram      = '256'

Vagrant.configure("1") do |config|
  config.vm.box = box
  config.vm.box_url = url
  config.vm.host_name = hostname + '.' + domain
  config.vm.network :hostonly, ip

  config.vm.share_folder("vagrant-root", "/vagrant", "./", :nfs => (RUBY_PLATFORM =~ /linux/ or RUBY_PLATFORM =~ /darwin/))

  config.vm.customize [
    'modifyvm', :id,
    '--name', hostname,
    '--memory', ram
  ]

  config.vm.provision :puppet do |puppet|
    puppet.manifests_path = 'puppet/manifests'
    puppet.manifest_file = 'site.pp'
    puppet.module_path = 'puppet/modules'
    puppet.options = ['--verbose']
  end
end
