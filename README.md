
## Introduction

Examples of Ansible

## Documentation

- https://ssh.guru/ansible-for-dummies-0-the-basics/
- https://github.com/geektechdude/ansible_container/blob/master/Dockerfile
- https://hub.docker.com/r/williamyeh/ansible/dockerfile
- https://www.redhat.com/sysadmin/container-images-ansible
- https://www.webcodegeeks.com/devops/docker-ansible-example/
- https://www.ansible.com/integrations/infrastructure
- https://medium.com/@golibraryco/infrastructure-as-code-orchestration-provisioning-configuration-management-ansible-7cd0615e49c5

## Execution

Prepare instances
```
docker-compose up 
```

Connection test between instances
```
docker exec -it aiac_manager /bin/bash
ansible-playbook -i /ansible/playbooks/test_files/hosts /ansible/playbooks/test_files/main.yml
```

Check the servers
```
docker exec -it aiac_server1 /bin/bash
cat /tmp/testAnsibleFile
cat /tmp/testAnsibleDir/copyOfAnsibleTestFile
```

```
docker exec -it aiac_server2 /bin/bash
cat /tmp/testAnsibleFile
cat /tmp/testAnsibleDir/copyOfAnsibleTestFile
```

TODO

- Make connection between instances without root
- Install nginx, php-fpm, mysql in separate instances
- Running all together
