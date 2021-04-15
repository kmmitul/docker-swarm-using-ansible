# docker-swarm-using-ansible
Here I have lunched two containers "Wildlfy" and "Postgres" on my target machine using Ansible playbook. The "main.yml" calss all the other yml file in order to complete the whole process. All the credentials like become passowrd or Postgress UID and password are saved in Ansible vault "Secret".

The Wildfly image is custom image also created by me. Please check  https://github.com/kmmitul/Custom-Wildfly-Image
