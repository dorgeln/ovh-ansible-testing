# ovh-ansible-testing

`pip install ovh`

`ansible-galaxy collection install git+https://github.com/dorgeln/infra-ovh-ansible-module`

# Create OVH API key

https://api.ovh.com/createToken/

# Get service name

https://api.ovh.com/console/#/cloud/project#GET

# Get SSH key
https://api.ovh.com/console/#/cloud/project/%7BserviceName%7D/sshkey#GET


# Encrypt your OVH secrets with ansible-vault use

`openssl rand -base64 32 > ~/.vault_pass.txt`

`ansible-vault create group_vars/all/ovh_secrets.yaml`

ovh_app_key: "Application Key"
ovh_app_secret: "Application Secret"
ovh_consumer_key: "Consumer Key"
ovh_service_name: "Service Name"
ovh_ssh_keyid: "SSH KEYID"


# Edit image config

group_vars/all/ovh_config.yaml

# Edit instance names

group_vars/all/ovh_instances.yaml


