# rdodockerdeploy
Ansible playbook for deploying RDO all-in-one, then converting the hypervisor type to 'Docker' in order to run containers as instances.

This was tested using a CentOS 7.1 host and takes care of all package updates before going through with the deployment.

**Installation**
- Enable EPEL repositories
- `sudo yum install -y ansible`

**Configuration**
- Modify `/etc/ansible/hosts` to include IP address for target Packstack server
- If you'd like to change the docker image used for testing, these variables are located in `roles/testcontainer/defaults/main.yml`

**Deployment**
- `ansible-playbook -s site.yml`

**Post-Deploy**

Once complete successfully there should be an instance named 'ansible_docker_instance' in the output of `nova list` on the packstack server. You will need to check the `keystonerc_admin` file on the packstack server to obtain admin credentials and log in to Horizon.
