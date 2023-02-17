# Week 0 — Billing and Architecture

## Required homework
```
Todo Checklist
	Watched Week 0 - Live Streamed Video	- [COMPLETED]
	Watched Chirag's Week 0 - Spend Considerations	- [COMPLETED]
	Watched Ashish's Week 0 - Security Considerations - [COMPLETED]
	Recreate Conceptual Diagram in Lucid Charts or on a Napkin	- [COMPLETED]
	Recreate Logical Architectual Diagram in Lucid Charts	- [COMPLETED]
	Create an Admin User	- [COMPLETED]
	Use CloudShell	- [COMPLETED]
	Generate AWS Credentials - [COMPLETED] 
	Installed AWS CLI - [COMPLETED]
	Create a Billing Alarm	- [COMPLETED] 
	Create a Budget - [COMPLETED]
```


# PROOF OF WORK (SEE BELOW)

## From Week0.md 
https://github.com/omenking/aws-bootcamp-cruddur-2023/blob/week-0/journal/week0.md

## <b>ENABLED MFA OF AWS(both root and IAM)</b>
I enabled MFA for both root user and IAM users.
![image](https://github.com/nullreturn/aws-bootcamp-cruddur-2023/blob/main/journal/assets/week0/mfaroot.png)


## Install AWS CLI [Completed]
Installed CLI for use with gitpod. I use powershell/azure CLI so its not unfamilar to me. Pretty useful for more complex tasks and scripting
![image](https://github.com/nullreturn/aws-bootcamp-cruddur-2023/blob/main/journal/assets/week0/gitpodstartup.png)
![image](https://github.com/nullreturn/aws-bootcamp-cruddur-2023/blob/main/journal/assets/week0/gitpodstartup2.png)


## "Update our .gitpod.yml to include the following task."
In gitpod, basically just followed the video by Andrew and modified my .yaml then pushed it. Now AWS cli will installed automatically for every new workspace within GitPod. Makes life much easier 
![image](https://github.com/nullreturn/aws-bootcamp-cruddur-2023/blob/main/journal/assets/week0/4yaml.png)

## Create a new User and Generate AWS Credentials
<sceenshot>

## Set Env Vars
Made the ENV Vars permamante so won't have to set them for each new workspace within Git
<img width="335" alt="printenv" src="https://user-images.githubusercontent.com/77585708/219153623-af1024bd-32df-444e-a6f9-e5afe51c8feb.png">

	
## AWS STS Caller
<img width="374" alt="sts" src="https://user-images.githubusercontent.com/77585708/219151915-0e2f8d30-3462-4931-9140-7282908ec7ca.png">


## Enable Billing
![image](https://github.com/nullreturn/aws-bootcamp-cruddur-2023/blob/main/journal/assets/week0/6billing.png)


## Billing Alarm
![image](https://user-images.githubusercontent.com/77585708/219156868-74b4582c-2dbf-4527-bbc1-cb08b0225c21.png)


## SNS TOPIC
![image](https://user-images.githubusercontent.com/77585708/219171637-965e74d3-2761-43e9-8b04-71511e9c4879.png)
![image](https://user-images.githubusercontent.com/77585708/219171866-475f84b6-9847-4dbe-8542-e31105d92c7f.png)
![image](https://user-images.githubusercontent.com/77585708/219172150-051e2575-087d-4153-9546-105fe2ce1ebb.png)


## Create Alarm
![image](https://user-images.githubusercontent.com/77585708/219176032-bb739992-3298-4272-af57-686eabb493f7.png)


## Create an AWS Budget
<screen shots>

## LUCID CHARTS - Cruddur Logic Diagram
![Cruddur Logic Diagram](https://user-images.githubusercontent.com/77585708/219173128-fbfc823a-3e18-4037-8a6e-2d52856e399a.png)

https://lucid.app/lucidchart/9b29ec5a-e75b-47a1-8942-52f778d6749c/edit?viewport_loc=-1840%2C-315%2C5120%2C2512%2C0_0&invitationId=inv_d4eae986-5832-4c6f-a09b-edbfd2093ce3
