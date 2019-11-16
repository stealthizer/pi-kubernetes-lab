# pi-kubernetes-lab


This code is related to the "How I meet your Cluster" blog series found in [part 1](https://dockernaut.wordpress.com/2018/03/26/how-i-meet-your-cluster-i/) and [part 2](https://dockernaut.wordpress.com/2018/05/28/how-i-meet-your-cluster-ii-kubernetes-on-arm-raspberry-pi-3/)

To setup the basic system, create a hosts file (you can use the example file provided) and execute:
```
ansible-playbook -k -i hosts base.yml
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

This Ansible playbooks are inspired in the works of [Ro14nd](https://ro14nd.de/kubernetes-on-raspberry-pi3)
