Elastic Container Services
[https://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_ContainerDefinition.html](https://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_ContainerDefinition.html)
[https://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_TaskDefinition.html](https://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_TaskDefinition.html)
It is to container what ec2 is to virtual machines.

2 modes : 
- EC2 
- Fargate 

ECS need : 
	- container definition : image & ports
- task definition: represents the application as a whole  (networking mode, hw requirements, cpu and co), Security (taskrole  ) + container ressources 
- task role: IAM role that the task assumes 
- service definition : define how the task can scale, add ha and resilience, restart 

Create Cluster -> deploy tasks/services into cluster