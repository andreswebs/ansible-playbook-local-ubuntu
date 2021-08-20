# ansible-playbook-local-ubuntu

An Ansible playbook to bootstrap a local Ubuntu system.

## Pre-requisites

Install Ansible:

```sh
sudo apt update
```
```sh
sudo apt install python3 python3-pip
```
```sh
python3 -m pip install --user ansible
```

Install Ansible roles:

```sh
ansible-galaxy install andreswebs.docker
```
```sh
ansible-galaxy install andreswebs.nodejs
```

## Run

Run the playbook on the localhost:

```sh
ansible-playbook ./playbook.yml \
  --extra-vars "custom_hosts=localhost current_user=$(whoami)" \
  --connection local \
  --ask-become-pass
```

## Authors

**Andre Silva** [@andreswebs](https://github.com/andreswebs)

## License

This project is licensed under the [Unlicense](UNLICENSE.md).
