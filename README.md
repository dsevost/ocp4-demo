# OpenShift 4 (beta) Installation and exploring

## Performing basic installation (libvirt)

1. Configure LibvirtD, NetworkManager, FirewallD according doc (https://github.com/openshift/installer/blob/master/docs/dev/libvirt-howto.md)
2. Build OpenShift Installer with LibvirtD support
3. Run OpenShift Installer with 'install-config' option
4. Fix LibvirtD Hypervisor's Network as you want (addressing, bridge name), masters and workers count
5. Runs OpenShift Installer with 'create' option
6. On final step of installation add dns record at LibvirtD network definition for host 'openshift-authentication-openshift-authentication.apps.<domain.tld>'

## Performing Cluster stratching (libvirt)

## Performing installation proceddure with Ansible'd playbooks

0. Prepare your ansible controller
``` 
vi inventories/work/hosts
ansible-playbook -i inventories/work/hosts 0-step
```

It fetches SSH finger prints of hypervisors and bastion, and creates admin user

