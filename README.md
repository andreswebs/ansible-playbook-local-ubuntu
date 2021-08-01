# ansible-playbook-local-ubuntu

An Ansible playbook to bootstrap a local Ubuntu system.

## Pre-requisites

Install Ansible:

```sh
sudo apt update
sudo apt install python3 python3-pip
python3 -m pip install --user ansible
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
