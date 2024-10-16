# gentoolab-ansible

My homelab ansible playbooks

> ⚠️ Use under your own risk

- [gentoolab-ansible](#gentoolab-ansible)
  - [Requeriments](#requeriments)
  - [How to use](#how-to-use)
    - [Generating encrypted random passwords using age](#generating-encrypted-random-passwords-using-age)

## Requeriments

- [Ansible](https://www.ansible.com/): an open source IT automation engine
- [age](https://github.com/FiloSottile/age): a simple, modern and secure file encryption tool

## How to use

Please refer to [Ansible](https://www.ansible.com) documentation on how to run Ansible playbooks.

Example command:

```bash
ansible-playbook -b -i ./your-local.inventory k3s/00-install-dependencies.playbook.yaml
```

### Generating encrypted random passwords using age

This one-liner will help you to generate a random password and encrypt it using age:

```bash
pwgen 16 1 > temp-password && age -R ~/.ssh/id_rsa.pub temp-password > ucarp.password.enc && rm temp-password
```

This will generate a 16 characters long password, encrypt it using your public key and save it to `ucarp.password.enc` file. You can then use this file in your playbooks.
