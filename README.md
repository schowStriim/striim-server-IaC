# Striim CI/CD Repository - Business Development
### The purpose of this CI/CD pipeline is to deploy PoC infrastructure/resources to all cloud providers (AWS, Azure, and Google Cloud).

1) Deploys Striim images to all cloud providers.
2) Deploys Striim server to AWS as an EC2 instance with the latest image attached.
3) Deploys instance scheduler infrastructure to AWS.
4) Defines the CI/CD pipeline using Github Actions tools.

### How to use this pipeline:
1) To deploy a new Striim image version to all cloud provider:
    - Click on 'Actions' tab.
    - Select 'Image builds pipeline' on the left panel.
    - Click on 'Run Workflow' dropdown, select 'main' branch to get the latest changes and then click on 'Run workflow' button.
 
2) To deploy/update a Striim EC2 instance with the latest image:
    - Click on 'Actions' tab.
    - Select 'Instance builds pipeline' on the left panel.
    - Click on 'Run Workflow' dropdown, select 'main' branch to get the latest changes and then click on 'Run workflow' button.
    
    To access and run the Striim server:
        - Ask your admin to provide you the striim_key.pem key.
        - Login to your AWS console and go to EC2 console.
        - Search for an instance named 'striim-server'.
        - Grab the ssh command after the 'Connect' button. (i.e. `ssh -i "<path>/<to>/<key>/striim_key.pem" ec2-user@ec2-54-213-129-76.us-west-2.compute.amazonaws.com`.
        - Execute the command in your terminal and enter 'yes' when it asks you to permanently save the hostname.