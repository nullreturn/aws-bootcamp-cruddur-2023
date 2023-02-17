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

## Create a new User and Generate AWS Credentials
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

## Set Env Vars
Made the ENV Vars permamante so won't have to set them for each new workspace within Git
![image](https://github.com/nullreturn/aws-bootcamp-cruddur-2023/blob/main/journal/assets/week0/7printenv.png)
	
## AWS STS Caller
ran aws sts get-caller... to prove who am I...
![image](https://github.com/nullreturn/aws-bootcamp-cruddur-2023/blob/main/journal/assets/week0/6sts.png)

## Enable Billing
I enabled Billing through AWS. Did it through Account settings and used my email. I will need to keep track of all expenses for this bootcamp.
![image](https://github.com/nullreturn/aws-bootcamp-cruddur-2023/blob/main/journal/assets/week0/6billing.png)


## Budgeting & Billing Alarm
Created a budget with both AWS site and through the CLI (watched the Andrew.. videos for that). Recieved an alarm to my email which I monitor
![image](https://github.com/nullreturn/aws-bootcamp-cruddur-2023/blob/main/journal/assets/week0/6bbillingalarm.png)
![image](https://github.com/nullreturn/aws-bootcamp-cruddur-2023/blob/main/journal/assets/week0/6cbudget.png)

## SNS TOPIC
Created an SNS topic in order to receive alarms when over billing occurs. Created with both AWS site and CLI 
![image](https://github.com/nullreturn/aws-bootcamp-cruddur-2023/blob/main/journal/assets/week0/10asns.png)
![image](https://github.com/nullreturn/aws-bootcamp-cruddur-2023/blob/main/journal/assets/week0/10snsconfirm.png)


## Create Alarm
Created an alarm. Confirmed alarm via email 
![image](https://github.com/nullreturn/aws-bootcamp-cruddur-2023/blob/main/journal/assets/week0/11snscreate.png)
![image](https://github.com/nullreturn/aws-bootcamp-cruddur-2023/blob/main/journal/assets/week0/snsconfirmed1.png)

## Cloud Trails
Created Cloud Trails to audit changes within AWS. Will be useful to do foresenics on any changes made
![image](https://github.com/nullreturn/aws-bootcamp-cruddur-2023/blob/main/journal/assets/week0/21trails.png)

## Orgization Units
Created OUs to divide users by departments. I'm familar with OUs from Active Directory and it seems the same in AWS
![image](https://github.com/nullreturn/aws-bootcamp-cruddur-2023/blob/9c6bb2c1b51a6325c7b01da55f34d0a1962659ba/journal/assets/week0/OU.png)

## Created SCP
useful to have OUs to divide departments and workflows. Prevented users from leaving OUs which I learned from Bootcamp
![image](https://github.com/nullreturn/aws-bootcamp-cruddur-2023/blob/main/journal/assets/week0/21aservicecontrols.png)

## EventBridge to hookup Health Dashboard to SNS and send notification
Now can receive health related alerts to SNS notificaitons and know when something goes down
![image](https://github.com/nullreturn/aws-bootcamp-cruddur-2023/blob/main/journal/assets/week0/99snseventbrig.png)

## Increasing service limits
https://docs.aws.amazon.com/servicequotas/latest/userguide/request-quota-increase.html
![image](https://github.com/nullreturn/aws-bootcamp-cruddur-2023/blob/main/journal/assets/week0/99qoutaincrease.png)
![image](https://github.com/nullreturn/aws-bootcamp-cruddur-2023/blob/main/journal/assets/week0/999pendingrequest.png)


## Well Architected Tool
<il>1. operational excellence<il>
<il>2. security</il>
<il>3. reliability</il>
<il>4. performance</il>
<il>5. cost optimization</il> 

## LUCID CHARTS - Cruddur Logic Diagram
![image](https://user-images.githubusercontent.com/77585708/219173128-fbfc823a-3e18-4037-8a6e-2d52856e399a.png)

https://lucid.app/lucidchart/9b29ec5a-e75b-47a1-8942-52f778d6749c/edit?viewport_loc=-1840%2C-315%2C5120%2C2512%2C0_0&invitationId=inv_d4eae986-5832-4c6f-a09b-edbfd2093ce3
