# gentoolab-ansible

My homelab ansible playbooks

> ⚠️ Use under your own risk

- [gentoolab-ansible](#gentoolab-ansible)
  - [Requeriments](#requeriments)
  - [How to use](#how-to-use)

## Requeriments

- [Ansible](https://www.ansible.com/): an open source IT automation engine
- [age](https://github.com/FiloSottile/age): a simple, modern and secure file encryption tool

## How to use

Please refer to [Ansible](https://www.ansible.com) documentation on how to run Ansible playbooks.

Example command:

```bash
ansible-playbook -b -i ./your-local.inventory k3s/00-install-dependencies.playbook.yaml
```