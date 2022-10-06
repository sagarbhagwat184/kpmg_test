
**3-tier Architecture**

In this folder you will see multiple cloud formation templates and 1 image of Architecture design which we are trying to achieve.

  Cloud formation Templates
	
      infra-kpmg.yml 
          This template will create following resource
              VPC
              Route Table
              Internet Gateway
              Attaches Internet Gateway to the VPC you just created
              2 Public Subnets
              Scaling Policy for Public Subnets
              Route Table for Public Subnets
              Associate the Public Subnets to the Route Table
              Security group with HTTP & SSH to open to 0.0.0.0/0
              Launch Template with Bootstrap script to install & launch Apache
              AutoScaling Group for Public Subnets
              Scaling Policy
              4 Private Subnets — two in us-east1a & two in us-east1b
              AutoScaling Group for two Private Subnets in the Application tier
        
	    database.yml
		       As file name suggested, it will have RDS instance and related configuration.
           
      network.yml
           This file will have all the network related resources.
