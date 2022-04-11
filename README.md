

<p align="center">
  <img 
    width="297"
    height="283"
    src="https://user-images.githubusercontent.com/21116260/161538444-987cb78a-b87e-4407-bae4-fa31ac42448b.png"
  >
</p>

# Project Overiew
This project Deploys a weight-tracker app image from a Control Node VM into Scale Set VMs which perform as agents over 2 environments: Staging and Production.

the infrastructure was created in Terraform and can be seen here:

https://github.com/liron-hazan/Weight-tracker-app-Terraform/edit/main/README.md


<p align="center">
  <img 
    width="801
    height="530
    src="https://user-images.githubusercontent.com/21116260/161540071-7dd769a8-f4f5-4e0f-9ccd-76d820388281.png">
</p>


## Main Components:
* 2x Load Balancer
* 2x VM + 1 scale set VM with 3 instances.
* 2x Managed Flexible PostgresQL DB Server

## Image Directory Structure:
<p align="center">
  <img 
    width="198
    height="467
    src="https://user-images.githubusercontent.com/21116260/161543664-153ff5f4-9be7-4289-a4ec-b252bbad5018.png">
</p>

All the files can be Cloned, Credential File excluded.

## installation Guide:
 1. Clone The project
 2. in the control node,place the main.yml file in the vars directory
 3. in folder's root, press ansible-playbook -i "inventory/<Chosen Enviornment>" --ask-become-pass main.yml
 4. enter the agents computer password.
 
 as a result, the script will be deplyed to the agents.



