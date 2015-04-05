
# ansible-role-clamav

Ansible role to install clamav antivirus and optionally ClamTK

# Installation

## Via galaxy

```bash
ansible-galaxy install igor_mukhin.clamav
```

## Manually

```bash
cd /path/to/roles
git clone https://github.com/ansible-roles/ansible-role-clamav.git igor_mukhin.clamav
```

# Example playbook

## Minimal example

```yml
- hosts: all
  roles:
    - igor_mukhin.clamav
```

## Install with ClamTK GUI for Ubuntu 13/14

```yml
- hosts: all
  vars:
    clamav_clamtk_install: true
  roles:
    - igor_mukhin.clamav
```

## Install with ClamTK GUI for Ubuntu 12

```yml
- hosts: all
  vars:
    clamav_clamtk_install: true
    clamav_clamtk_url: "https://bitbucket.org/dave_theunsub/clamtk-legacy/downloads/clamtk_5.15-1.legacy_all.deb"
  roles:
    - igor_mukhin.clamav
```

## What if you using KDE?

```yml
- hosts: all
  vars:
    clamav_clamtk_install: true

    # Specify KDE GUI package URL:
    clamav_clamtk_url: https://bitbucket.org/dave_theunsub/clamtk-kde/downloads/clamtk-kde_0.16-1_all.deb

  roles:
    - igor_mukhin.clamav
```

# Testing

```bash
cd tests && vagrant up
```

# License

MIT
