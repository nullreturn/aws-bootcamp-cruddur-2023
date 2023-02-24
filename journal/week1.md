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
  

  
  ## <b>HOMEWORK</b>

## Run the dockerfile CMD as an external script
- Modified the dockerfile to use RUN python ./python3flask.py instead of CMD
- it ran but had to fiddle around a bit 
  ![image](https://user-images.githubusercontent.com/77585708/221247403-1f8e2eab-31a1-4da2-89a0-e2242550834f.png)

  
## Push and tag a image to DockerHub (they have a free tier)
- Created a dockerhub account
- then I built an image and pushed it with a tag to dockerhub
- see screens and link below
  
  
![1dockerpushimagecorrect](https://user-images.githubusercontent.com/77585708/220498272-8bad2296-1c91-427d-a401-ee04d6cd9df8.png)
![2dockerpushcorrect](https://user-images.githubusercontent.com/77585708/220498278-229cf9ef-100a-4732-8cb3-b10da11d0616.png)
![3dockerpushcorrect](https://user-images.githubusercontent.com/77585708/220498316-af490a5b-84f8-416c-8f58-8c6f8f08f54d.png)
  https://hub.docker.com/r/containofcontainers/awsbootcamp

##Use multi-stage building for a Dockerfile build

## Implement a healthcheck in the V3 Docker compose file
I added healthchecks with  my docker-compose.yaml following documention from Docker. It will use curl to contact the the backend,frontend, and the database with different invertal,time out, and retries. I will have to play around with the values to make sure its appropriate for the service 
  ![image](https://user-images.githubusercontent.com/77585708/221296704-4fd6d310-0eee-4ee9-9b51-c1b1911e3f03.png)
I"m able to check docker docker ps. I can look further down the line to add it to some logging/siem solution to get alerts
![image](https://user-images.githubusercontent.com/77585708/221296948-5187ce35-d8de-4085-88b8-35b5dbe2955e.png)


  
## Research best practices of Dockerfiles and attempt to implement it in your Dockerfile

## Learn how to install Docker on your localmachine and get the same containers running outside of Gitpod / Codespaces
I have a Macbook with OSX so I've used that as a localmachine.
- installed Docker
- installed homebrew and npm
- used github clone my repo
- made changes in my firewall so didn't have to worry about ports
- used docker-compose up -d and also Visual Code studio (testing it out - pretty much the same as gitpod.io)
- Then, was able to get the docker containers working 
  
  
## Launch an EC2 instance that has docker installed, and pull a container to demonstrate you can run your own docker processes. 
- I've created an EC2 Ubuntu instance with free tier settings
- allowed http/https/and other ports just for sake of the lab
- ssh into the aws box
- updated packages, installed docker then picked midnight commander in docker hub since its an easy demo
- and the obligatory neofetch screenshot
<img width="400" alt="2neofetch" src="https://user-images.githubusercontent.com/77585708/220981382-bb886fba-ec7c-402d-928f-ee013fc28f13.png">
<img width="529" alt="3dockerinstallrun" src="https://user-images.githubusercontent.com/77585708/220981413-2c50f5c7-8d1d-4fe1-8119-80eb9b8263d4.png">
<img width="578" alt="4mcrunning" src="https://user-images.githubusercontent.com/77585708/220981432-9d4d47dd-15f6-4c4a-8053-db6b1b26cbac.png"> 
![1docker](https://user-images.githubusercontent.com/77585708/221073523-d9b3a8e2-f696-433f-b2c9-53ad05599383.png)
![2docker](https://user-images.githubusercontent.com/77585708/221073592-74e1c70e-bb1f-48ef-a261-f1de02375340.png)
![4docker](https://user-images.githubusercontent.com/77585708/221073644-ee99b06b-05e9-4bf6-bc8d-33efc6e9f014.png)
![3dockrt](https://user-images.githubusercontent.com/77585708/221073680-6b7857b3-d517-4695-ae8e-f48f3ec7288e.png)
