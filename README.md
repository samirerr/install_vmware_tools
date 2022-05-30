# Ansible Role: vmwaretools

This role will help you with installing vmware-tools via yum or source.

## Requirements

None.

## Role Variables

Depending on installation some arguments may differ.
__Check the default variables for precise comment about ths role interface.__

Common required args are:
```yaml
# The package of VMware Tools to install. 
vmwaretools_pkg: open-vm-tools
# The source of VMware Tools to install. 
vmtools_install_method:  yum
```
```yaml
# The package of VMware Tools to install. 
vmwaretools_pkg: vmtools.tgz
# The source of VMware Tools to install. 
vmtools_install_method:  source

```

## Dependencies

None.

## Example Playbook

```yaml
- hosts: servers
  become: yes
  roles:
    - role: install_vmware_tools 
      vars:
        vmtools_install_method: source
        vmtools_pkg: vm.tgz
        user_appliance: root
        dest_pkg: /tmp
```

## Author Information

This role was created in 2022 by [rania.ben.halima@kyndryl.com](mailtorania.ben.halima@kyndryl.com)
# test_vmtools
# install_vmware_tools
