Installing Ansible Module for Usage for RHEL
====================

Requirements: 
This collection has been tested against following Ansible versions: >=2.9.17. 

Python Support-Collection supports 3.6+

Installing: 
ansible-galaxy collection install kubernetes.core or community.kubernetes

pip3 install kubernetes
    pip will install this package: https://pypi.org/project/kubernetes/


Running the Playbook 
====================

The playbook will onboard a team to a cluster or delete a team from a cluster 

1. Onboard the team a cluster: 
```
ansible-playbook playbook.yaml -t create -e @non-prod-vars.yaml
```
2. Delete a Team from a cluster:
```
ansible-playbook playbook.yaml -t delete -e @non-prod-vars.yaml
```

Vars File
=========
a vars file is required to specify namespace attributes
```
app: danny
developers: minotaurs
leads: leaders 
viewers: just-see   
namespaces: 
  - env: dev
    size: small
  - env: qa
    size: medium
```
