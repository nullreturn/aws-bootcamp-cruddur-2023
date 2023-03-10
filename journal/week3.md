# Week 3 — Decentralized Authentication


### Example below of trying to sign in provisioned user in Amazon Cognito User Pool
I put xxxxxxx in the screenshot but there is a real username. The user was manually provivsioned  
![image](https://github.com/nullreturn/aws-bootcamp-cruddur-2023/blob/main/journal/assets/week3/1cannotlogin.png)
### manually provisioned user logged in
![image](https://github.com/nullreturn/aws-bootcamp-cruddur-2023/blob/main/journal/assets/week3/2successlogin.png)

### after allow users to create their acocunt 
- ran into issue where had to use AWS terminal to reset the users password in order before loggging in 
the user is able to register/join within the Cruddur site, after they do an email veriftiction code is sent to them
![image](https://github.com/nullreturn/aws-bootcamp-cruddur-2023/blob/main/journal/assets/week3/3confirmationpage.png)

### AWS Cognito pool users that have been created by the end users themselves
see confirmation status
one of the users' password was reset via AWS STS terminal command
![image](https://github.com/nullreturn/aws-bootcamp-cruddur-2023/blob/main/journal/assets/week3/4confirmeduser.png)

### Cognito user signed in
![image](https://github.com/nullreturn/aws-bootcamp-cruddur-2023/blob/main/journal/assets/week3/5userloggedin.png)

### Password reset in action 
![image](https://github.com/nullreturn/aws-bootcamp-cruddur-2023/blob/main/journal/assets/week3/6recovery.png)
