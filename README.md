# docker-swarm-using-ansible
Here I have deployed two containers namely "Wildlfy" and "Postgres" inside of my Docker Swarm cluster running on my target machines using Ansible playbook. 

- Install_Docker.yml ---> Preapre the Docker Environment on the nodes of my cluster.
- Initialize_Cluster.yml --> Prepare my master node to initialiye the cluster.
- Add_Nodes.yml ---> Add my worker node with the master node.
- Run_Containers_In_Cluster.yml ---> Run my containers with replicas and healthcheck
- portainer.yml ---> Deploy Portainer stack on master node to have a nice container management GUI

The "main.yml" calls all the other yml file in order to complete the whole process. All the credentials like become passowrd or Postgress UID and password are saved in Ansible vault "Secret".

The Wildfly image is custom image also created by me. Please check  https://github.com/kmmitul/Custom-Wildfly-Image
