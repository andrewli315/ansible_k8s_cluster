## Ansible playbook for k8s cluster installation

### Usage
* create the inventory.ini
```
[cp]
{ip}

[nodes]
{ip}
{ip}
{ip}
```
* create the hosts file to alternate the vm's /etc/hosts file
```
{ip} dk8scp1
{ip} dk8snode1
{ip} dk8snode2
{ip} dk8snode3

```
* execute ansible-playbook
`ANSIBLE_HOST_KEY_CHECKING=False ansible-playbook install_k8s_nodes.yml -i inventory.ini --extra-vars "cp_ip={cp_ip}"`



