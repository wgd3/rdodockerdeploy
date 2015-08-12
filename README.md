# rdodockerdeploy
Ansible playbook for deploying RDO all-in-one then converting the hypervisor to support Docker container.

This was tested using a CentOS 7.1 host and takes care of all package updates before going through with the deployment.

Current Caveats:
- https://bugs.launchpad.net/nova/+bug/1461217
- https://bugzilla.redhat.com/show_bug.cgi?id=997290
