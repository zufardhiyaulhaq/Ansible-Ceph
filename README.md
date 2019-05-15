# Ansible Ceph
Ansible Playbook to create Ceph Storage Cluster in CentOS

### Testing in
* 1 Ceph mon
* 3 Ceph node
* CentOS 7.6

### Instalation
* Prepare deployer nodes (ansible is installed in here)
```
sudo apt-add-repository ppa:ansible/ansible
sudo apt update
sudo apt install ansible
```
* Make sure deployer have root access into all nodes (tips using ssh-copy-id)
```
ssh-copy-id root@ceph-node
```
* Clone Repository
```
git clone https://github.com/zufardhiyaulhaq/Ansible-Ceph.git
```
* Edit Variables
```
hosts/hosts
group_vars/all.yml
```
* Run ansible
```
ansible-playbook main.yml -i hosts/hosts
``` 