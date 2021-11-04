# ovh-ansible-testing

## Install dependencies 

`pip install ovh ansible`
`ansible-galaxy collection install git+https://github.com/dorgeln/infra-ovh-ansible-module`
`ansible-galaxy install maresb.micromamba`
`ansible-galaxy install geerlingguy.docker`


## Create OVH API key

https://api.ovh.com/createToken/

## Get service name

https://api.ovh.com/console/#/cloud/project#GET

## Get SSH key
https://api.ovh.com/console/#/cloud/project/%7BserviceName%7D/sshkey#GET


## Encrypt your OVH secrets with ansible-vault use

`openssl rand -base64 32 > ~/.vault_pass.txt`

`ansible-vault create group_vars/all/ovh_secrets.yaml`

```
ovh_app_key: "OVH Application Key"
ovh_app_secret: "OVH Application Secret"
ovh_consumer_key: "OVH Consumer Key"
ovh_service_name: "OVH Service Name"
ovh_ssh_keyid: "SSH KEYID"
```

`ansible-vault create group_vars/all/github_secrets.yaml`

```
github_token: "Personal access tokens"
```

## Edit image config

group_vars/all/ovh_config.yaml

## Edit instance names

group_vars/all/ovh_instances.yaml


eval "$(micromamba shell hook --shell=bash)"
micromamba activate --prefix=~/.microforge

ansible-playbook ovh.yml



