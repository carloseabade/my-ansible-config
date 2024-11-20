<div align="center">

[![My Ansible Config][ansible_logo]][repo_url]

# My Ansible Config

A quick way of **seting up a new computer** with the **same packages and configuration**.

</div>

## Quick start

Clone the repo to your computer:

```bash
git clone https://github.com/carloseabade/my-ansible-config
```

Run your playbook:

```bash
ansible-playbook playbook.yml -i HOST_IP, -e ansible_ssh_private_key_file=PATH_TO_PRIVATE_KEY
```

> You can run on localhost by not passing -i and -e:
> ansible-playbook playbook.yml -i localhost,

<!-- Repository -->

[ansible_logo]: https://raw.githubusercontent.com/ansible/logos/refs/heads/main/vscode-ansible-logo/vscode-ansible.png
[repo_url]: https://github.com/carloseabade/my-ansible-config
