# personal-vps

Configure a Virtual Private Server using Ansible.

## Configure

Install `devsec.hardening` Ansible collection

```bash
ansible-galaxy collection install devsec.hardening
```

## Ansible

Ansible will:

- TBD

### Running

Ping all dev servers

```sh
$ ansible-playbook ./playbooks/ping.yaml -i inventory -l dev
```

Check what will be changed on the dev server(s)

```sh
$ ansible-playbook ./playbooks/setup.yaml -i inventory -l dev --check
```

Run setup tasks on all dev servers

```sh
$ ansible-playbook ./playbooks/setup.yaml -i inventory -l dev
```

Run hardening tasks on all dev servers

```sh
$ ansible-playbook ./playbooks/hardening.yaml -i inventory -l dev --tags="yum"
```

Install and configure OpenVPN on all dev servers

```sh
$ ansible-playbook ./playbooks/openvpn.yaml -i inventory -l dev
```
