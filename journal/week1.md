## Class Summary
Create a new GitHub repo
Launch the repo within a Gitpod workspace
Configure Gitpod.yml configuration, eg. I’m VSCode Extensions
Clone the frontend and backend repo
Explore the codebases
Ensure we can get the apps running locally
Write a Dockerfile for each app
Ensure we get the apps running via individual container
Create a docker-compose file
Ensure we can orchestrate multiple containers to run side by side
Mount directories so we can make changes while we code


# Week 1 — App Containerization
![image](https://github.com/nullreturn/aws-bootcamp-cruddur-2023/blob/main/journal/assets/week1/1pip3running.png)

## Containerize Backend


### Run Python
![image](https://github.com/nullreturn/aws-bootcamp-cruddur-2023/blob/main/journal/assets/week1/1pip3running.png)
![image](https://github.com/nullreturn/aws-bootcamp-cruddur-2023/blob/main/journal/assets/week1/6run.png)

## Add Dockerfile


## Add Dockerfile


## Build Container
![7bsuccess](https://user-images.githubusercontent.com/77585708/219995169-269d4575-aea6-42b9-b487-2a0d1ed7ceda.png)

## Run container
container running with 
![image](https://user-images.githubusercontent.com/77585708/220182039-e851c98b-7a73-4a2e-abaa-684bda7281b7.png)
![image](https://user-images.githubusercontent.com/77585708/220182142-9eff27a8-477a-4466-87fb-34a4489241f5.png)

##Get Container Images or Running Container Ids
can check if docker is a running process
''
docker ps
''
![image](https://user-images.githubusercontent.com/77585708/220184972-8a880e1a-d5a7-44b2-8fae-582a2d565983.png)

check running docker images
''docker image''
![image](https://user-images.githubusercontent.com/77585708/220185060-aae3c657-a25d-46fb-8bc8-07cff4cd6dc0.png)


## Send Curl to Test Server
grabs content from webpage and oututs to console
''
curl -X GET http://localhost:4567/api/activities/home -H "Accept: application/json" -H "Content-Type: application/json"
''

### 
<img width="1229" alt="10dockercomposefrontend1" src="https://user-images.githubusercontent.com/77585708/219997647-0c33e2cd-d645-4af7-bcb8-5c22fa3bf153.png">
![cbrundocker](https://user-images.githubusercontent.com/77585708/219997855-6acaceb4-e762-4343-a120-7bfc466a134c.png)



## Containerize Frontend
<screeenshot1>


## Run NPM Install

notication tabs is not working so will have to  need to add endpoint for notificaiton tabs









## homework
Run the dockerfile CMD as an external script
Push and tag a image to DockerHub (they have a free tier)
Use multi-stage building for a Dockerfile build
Implement a healthcheck in the V3 Docker compose file
Research best practices of Dockerfiles and attempt to implement it in your Dockerfile
Learn how to install Docker on your localmachine and get the same containers running outside of Gitpod / Codespaces
Launch an EC2 instance that has docker installed, and pull a container to demonstrate you can run your own docker processes. 

