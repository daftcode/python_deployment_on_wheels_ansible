EXAMPLE Python WHEEL Deployemnt Playbook
========================================

[Ansible](http://ansible.com) Playbook example of **test_app** deployment

1. Clone this repo
2. Edit hosts and variables
3. Run desired play

Ansible play run command template:
ansible-playbook -i hostsfile <app>.yml --vault-password-file ./pass


This play was writtent as an example for [Ansible Python web apps deployment on wheels](https://blog.daftcode.pl/) article by me (webster58). Play alone is useless without an app wchich is not provided at this stage, but the idea of Wheel deployment is for You to use.

examples

**TEST_APP Full Deployment**:
> ansible-playbook -i production_hosts test_app.yml --vault-password-file ./pass

**TEST_APP Tagged Config Deployemnt**:
> ansible-playbook -i production_hosts test_app.yml --vault-password-file ./pass -t config

**TEST_APP Different branch Deployment**:
> ansible-playbook -i production_hosts test_app.yml --vault-password-file ./pass --extra-vars "app_git_branch=stage"

**TEST_APP Stageing Deployment**:
> ansible-playbook -i stage_hosts test_app.yml --vault-password-file ./pass -t app --extra-vars "app_git_branch=stage"
