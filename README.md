# ansible-playbook-local-ubuntu

An Ansible playbook to bootstrap a local Ubuntu system.

## Pre-requisites

Install Ansible:

```sh
sudo apt update
```

```sh
sudo apt install python3 python3-pip python3-venv
```

```sh
python3 -m venv .python-env
source .python-env/bin/activate
pip install --user ansible
```

Install Ansible requirements:

```sh
ansible-galaxy install -r requirements.yml
```

## Run

Run the playbook on the localhost:

```sh
ansible-playbook ./playbook.yml \
  --extra-vars "custom_hosts=localhost current_user=$(whoami)" \
  --connection local
```

Note: add `--ask-become-pass` if the user doesn't have passwordless `sudo`.

## Authors

**Andre Silva** [@andreswebs](https://github.com/andreswebs)

## License

This project is licensed under the [Unlicense](UNLICENSE.md).
