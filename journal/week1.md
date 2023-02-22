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

## run docker background
''
docker run --rm -d -p 4567:4567 -it -e FRONTEND_URL='*' -e BACKEND_URL='*' backend-flask
''

check running docker images
''docker image''
![image](https://user-images.githubusercontent.com/77585708/220185060-aae3c657-a25d-46fb-8bc8-07cff4cd6dc0.png)

## kill docker
docker kill [docker name] 
get name from docker ps

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


### Backend notification endpoint changes

created a notifications_activites.py in order to create notification funciton, in backend-flask and used home_activities as a template.

<screenshots>


### Frontend notifications endpoint changes
Frontend uses react client then mounts the app into root. React router handles all the route. A new page had to be created in app.js so React will know how to route it 
<screen5>

I had to create the notificationpage because import NotificationsFeedPage from './pages/NotificationsFeedPage' did not exist within /pages along with a .css

## final results of 
  ![image](https://user-images.githubusercontent.com/77585708/220458672-2f52926b-92de-4a87-9dd1-e7bf98e9b642.png)


## creating a table to test if dynmo db works
![image](https://user-images.githubusercontent.com/77585708/220461951-dac64e8e-3aeb-4546-8726-13b9d8ebe7b1.png)

 code used from 100 days of cloud.. returns output indicating that the records have been created 

  ##item has been created
![image](https://user-images.githubusercontent.com/77585708/220462252-feff4ba3-ed8d-43e3-a581-598cb1b0be24.png)

 ## listing tables
![image](https://user-images.githubusercontent.com/77585708/220462405-58d1b47f-5f9c-439a-b283-345920fcfa8d.png)
output shows that a table has been created 

 ## Get records

  ![image](https://user-images.githubusercontent.com/77585708/220462711-0820bcf3-8fe9-4120-81cf-14d30aebdc71.png)
 
  ## Postgres
  
  database explorer test
![image](https://user-images.githubusercontent.com/77585708/220466250-7ffc1ec8-9fb2-4469-8039-4961576f5dcd.png)

  ##postgres cleint connecting terminal
have to specify localhost in order to connect 
  ![image](https://user-images.githubusercontent.com/77585708/220467399-e34210c6-a340-4f67-96ce-a7e1c59bc41c.png)
  

  
## homework
Run the dockerfile CMD as an external script

## Push and tag a image to DockerHub (they have a free tier)
![1dockerpushimagecorrect](https://user-images.githubusercontent.com/77585708/220498272-8bad2296-1c91-427d-a401-ee04d6cd9df8.png)
![2dockerpushcorrect](https://user-images.githubusercontent.com/77585708/220498278-229cf9ef-100a-4732-8cb3-b10da11d0616.png)
![3dockerpushcorrect](https://user-images.githubusercontent.com/77585708/220498316-af490a5b-84f8-416c-8f58-8c6f8f08f54d.png)

  Use multi-stage building for a Dockerfile build
Implement a healthcheck in the V3 Docker compose file
Research best practices of Dockerfiles and attempt to implement it in your Dockerfile
Learn how to install Docker on your localmachine and get the same containers running outside of Gitpod / Codespaces
Launch an EC2 instance that has docker installed, and pull a container to demonstrate you can run your own docker processes. 

