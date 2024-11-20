<div align="center">

[![My Ansible Config][ansible_logo]][repo_url]

# My Ansible Config

A quick way of **seting up a new computer** with the **same packages and configuration**.

</div>

## Quick start

> Prerequisites: you need to be able to connect to the host machine using ssh. Check [prerequisites](#prerequisites) for more info.

Clone the repo to your controller machine:

```bash
git clone https://github.com/carloseabade/my-ansible-config
```

Run your playbook against your target machine:

```bash
ansible-playbook playbook.yml -i HOST_IP, -e ansible_ssh_private_key_file=PATH_TO_PRIVATE_KEY
```

> You can run on localhost by not passing `-e` and using `localhost` on `-i`:
> ansible-playbook playbook.yml -i localhost,

## Prerequisites

On the target machine, install `openssh-server`.

```bash
sudo apt install openssh-server -y
```

On the controller machine, generate an SSH key pair.

```bash
ssh-keygen -t ed25519
```

Then, copy the public key to the target machine.

```bash
ssh-copy-id USER@HOST
```

Check if you can SSH into the target machine.

```bash
ssh USER@HOST
```

> For more information about SSH in general, [ssh.com][ssh_academy] is a great resource.

<!-- Repository -->

[ansible_logo]: https://raw.githubusercontent.com/ansible/logos/refs/heads/main/vscode-ansible-logo/vscode-ansible.png
[repo_url]: https://github.com/carloseabade/my-ansible-config


<!-- External -->

[ssh_academy]: https://www.ssh.com/academy/ssh-keys
