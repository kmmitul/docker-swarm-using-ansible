# Deploying Docker Swarm using Ansible
Here I have deployed two containers namely "Wildlfy" and "Postgres" in a Docker Swarm cluster running on my target machines using Ansible playbook. 

![image](https://user-images.githubusercontent.com/59294204/114857346-71135d00-9de8-11eb-93db-c006dce467e8.png)

-	Install_Docker.yml ---> Prepares the Docker environment on the nodes or target machines.
-	Initialize_Cluster.yml --> Prepares master node to initialize the cluster.
-	Add_Nodes.yml ---> Adds worker node(s) with the master node.
-	Run_Containers_In_Cluster.yml ---> Deploys my custom WildFly containers into the cluster.
-	Swirl.yml ---> Deploys Swirl container to provide a swarm management user interface
-	Prometheus_all.yml ---> Deploy Prometheus along with cAdvisor to integrate with Swirl for visualizing container metrics using my custom Prometheus image
- secret.yml ---> All the credentials like become passowrd or Postgress UID and password are saved in this Ansible vault.
- ansible.cfg --> Ansible Configuration file 
- inventory --> Ansible Inventory file

The Wildfly image used in this project, is a custom image also created by me. Please check  https://github.com/kmmitul/Custom-Wildfly-Image
