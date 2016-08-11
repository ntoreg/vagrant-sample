Dotenv.load

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.provider :cloudstack do |cloudstack, override|
    override.vm.box     = "dummy"
    override.vm.box_url = "https://github.com/klarna/vagrant-cloudstack/raw/master/dummy.box"

    # endpoint
    cloudstack.scheme = "https"
    cloudstack.host = "#{ENV['CS_HOST']}"
    cloudstack.port = "443"
    cloudstack.path = "/client/api"

    # api key
    cloudstack.api_key = "#{ENV['CS_API_KEY']}"
    cloudstack.secret_key = "#{ENV['CS_SECRET_KEY']}"

    # network parameters
    cloudstack.network_type = "Advanced"
    cloudstack.zone_name = "#{ENV['CS_ZONE']}"
    cloudstack.network_name = "#{ENV['CS_NETWORK']}"
    cloudstack.pf_ip_address = "#{ENV['CS_PF_IP_ADDRESS']}"
    # cloudstack.pf_ip_address_id = "#{ENV['CS_PF_IP_ADDRESS_ID']}"
    cloudstack.pf_public_port = "#{ENV['CS_PF_PUBLIC_PORT']}"
    cloudstack.pf_private_port = "22"

    # vm parameters
    cloudstack.name = "#{ENV['VM_NAME']}"
    cloudstack.display_name = "#{ENV['VM_DISPLAY_NAME']}"
    cloudstack.template_name = "#{ENV['CS_TEMPLATE']}"
    cloudstack.service_offering_name = "#{ENV['CS_SERVICE_OFFERING']}"
    cloudstack.keypair = "#{ENV['CS_SSH_KEYPAIR']}"

    # override
    override.ssh.username = "#{ENV['VAGRANT_SSH_USERNAME']}"
    override.ssh.private_key_path = "#{ENV['VAGRANT_SSH_PRIVATE_KEY']}"
    override.ssh.port = "#{ENV['CS_PF_PUBLIC_PORT']}"
  end
end
