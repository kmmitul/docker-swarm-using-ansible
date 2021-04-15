# Deploying Docker Swarm using Ansible
Here I have deployed two containers namely "Wildlfy" and "Postgres" in a Docker Swarm cluster running on my target machines using Ansible playbook. 

- main.yml --> calls all other Ansible playbook files in a orderly manner to complete the whole process.
- Install_Docker.yml ---> Preapre the Docker Environment on the nodes of my cluster.
- Initialize_Cluster.yml --> Prepare my master node to initialiye the cluster.
- Add_Nodes.yml ---> Add my worker node with the master node.
- Run_Containers_In_Cluster.yml ---> Run my containers with replicas and healthcheck
- portainer.yml ---> Deploy Portainer stack on master node to have a nice container management GUI
- secret.yml ---> All the credentials like become passowrd or Postgress UID and password are saved in this Ansible vault.
- ansible.cfg --> Ansible Configuration file 
- inventory --> Ansible Inventory file

The Wildfly image used in this project, is a custom image also created by me. Please check  https://github.com/kmmitul/Custom-Wildfly-Image
