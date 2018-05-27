# pi-kubernetes-lab


This code is related to the "How I meet your Cluster" blog series found in part 1 and part 2

To setup the basic system, create a hosts file (you can use the example file provided) and execute:
```
ansible-playbook -k -i hosts setup.yml
```
To create the master node, execute:
```
ansible-playbook -i hosts kubeadm-master.yml
```
To add slave nodes to the cluster, execute:
```
ansible-playbook -i hosts kubeadm-slaves.yml
```
If something goes wrong, you can reset the kubernetes installation by executing:
```
ansible-playbook -i hosts kubernetes-full-reset.yml
```
To power down everything you can execute:
```
ansible-playbook -i hosts Shutdown.yml
```

This Ansible playbooks are inspire in the works of [Ro14nd](https://ro14nd.de/kubernetes-on-raspberry-pi3)