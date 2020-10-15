# ansible-galaxy repo-epel examples

## Prerequisite

* `yaml-lint` is installed
* `ansible-lint` is installed
* `ansible` is installed

## Example - `geerlingguy.repo-epel`

### Install it

```sh
ansible-galaxy role install `geerlingguy.repo-epel`
```

Create a playbook `main.yml` with the following content:

```yml
---
- name: Playbook to install repo-epel on a RHEL or CentOS linux machine.
  hosts: all
  roles:
    - role: geerlingguy.repo-epel

```

Check it with `yamllint`

```sh
yamllint .
```

Check playbook syntax with `--syntax-check` option

```sh
ansible-playbook main.yml --syntax-check
```

Check it with `ansible-lint`

```sh
ansible-lint .
```

Run playbook `main.yml`

```sh
ansible-playbook main.yml
```

### Verify using `Vagrant`

```sh
vagrant up

# Atfer the VM is up run vagrant provision
vagrant provision
```

### Cleanup

```sh
vagrant destroy -f
```
