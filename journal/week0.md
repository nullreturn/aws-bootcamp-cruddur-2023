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

## Created IAM USER
best practice not to work out of the ROOT account and use an IAM with assigned groups/policies. Followed the videos and did so. Have a user that has admin group and access to billing. Created another user later on for just read access (accesing logs& audits after) 
![image](https://github.com/nullreturn/aws-bootcamp-cruddur-2023/blob/main/journal/assets/week0/5iamusers.png)


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


## Budgeting & Billing Alarm
![image](https://github.com/nullreturn/aws-bootcamp-cruddur-2023/blob/main/journal/assets/week0/6bbillingalarm.png)
![image](https://github.com/nullreturn/aws-bootcamp-cruddur-2023/blob/main/journal/assets/week0/6cbudget.png)

## SNS TOPIC
![image](https://github.com/nullreturn/aws-bootcamp-cruddur-2023/blob/main/journal/assets/week0/10asns.png)
![image](https://github.com/nullreturn/aws-bootcamp-cruddur-2023/blob/main/journal/assets/week0/10snsconfirm.png)


## Create Alarm
![image](https://github.com/nullreturn/aws-bootcamp-cruddur-2023/blob/main/journal/assets/week0/11snscreate.png)

## Cloud Trails
![image](https://github.com/nullreturn/aws-bootcamp-cruddur-2023/blob/main/journal/assets/week0/21trails.png)
![image](https://github.com/nullreturn/aws-bootcamp-cruddur-2023/blob/main/journal/assets/week0/21aservicecontrols.png)

## LUCID CHARTS - Cruddur Logic Diagram
![Cruddur Logic Diagram](https://user-images.githubusercontent.com/77585708/219173128-fbfc823a-3e18-4037-8a6e-2d52856e399a.png)

https://lucid.app/lucidchart/9b29ec5a-e75b-47a1-8942-52f778d6749c/edit?viewport_loc=-1840%2C-315%2C5120%2C2512%2C0_0&invitationId=inv_d4eae986-5832-4c6f-a09b-edbfd2093ce3
