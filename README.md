##Update - 8/12 

- Basic support for Windows VMs added.
- Dialog now has option to set password for VM, choose OS type type (Windows or Linux), and select instance size


##Updated 7/31 

* The following variables are now provided from the VMDB:

  * Hyper-V host credentials
  * Azure provider credentials

* The following are user supplied via dynamic dialogs:
  * Azure resource group
  * Azure storage account 
  * Azure network
  * Azure subnet

*  Users can now enter the name for their public IP & network interface resources.

## Contents of repo:

1. JMR(directory) - the unzipped automate domain contents
2. ansible-playbook(dir) - directory containing the ansible playbook to prep the VM for migration
3. datastore*.zip - Dump of the automate code from the CFME UI, for import via UI into another environment
4. dialog_*.yml - Export of service dialogs for getting resource groups, storage accounts, or both via automate


## Next steps:  

* Add support for other Linux distros to the Ansible playbook - I think at a minimum, I'll need to account for different installation methods with regard to the Azure agent (ie apt vs yum)
* Begin working with other on-prem virt providers.  I'm probably going to prioritize RHEV over OpenStack or VMWare as I already have it setup in my lab.
  