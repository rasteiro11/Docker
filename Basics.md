# How To Install Docker in Ubuntu Server
---
1. cd /
2. sudo apt-get update
3. sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
    software-properties-common
4. curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
5. sudo apt-key fingerprint 0EBFCD88
6. sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   eoan \
   stable"
7. sudo apt-get update
8. sudo apt-get install docker-ce docker-ce-cli containerd.io
9. sudo usermod -aG docker your-user
10. docker run hello-world
    
---
# Basic Commands In Docker
- --
### `Run a Container`
- docker run <span style="color: blue">image name</span>
- --
### `List Running Containers`
- docker ps
- --
### `List Every Container Ever Created`
- docker ps --all
- --
### `Docker Run in Depth`
 - docker run = docker create <span style="color: blue">image name</span> + docker start <span style="color: red">container id</span>
 - --
 ### `Create A Container`
 - docker create <span style="color: blue">image name</span> 
- --
### `Start a Container`
- docker start <span style="color: red">container id</span> <- <strong>do not return feedback from terminal</strong>

- docker start <span style="color: red">container id</span> -a <- <strong>return feedback from terminal</strong>
- --
### `Delete Stopped Containers`
- docker system prune
- --
### `Get Logs From Container`
- docker logs <span style="color: red">container id</span>
- --
### `Stop a Container`
- docker stop <span style="color: red">container id</span>
- --
### `Kill a Container`
- docker kill <span style="color: red">container id</span> <- <strong>Kills the Container At the Moment</strong>
- --
### `Execute an Additional Command in a Container`
- docker exec -it <span style="color: red">container id</span> <span style="color: yellow">command</span>
- <b>-it</b> means that the container can recieve input 
- --
### `Command Prompt inside a Container`
- docker exec -it <span style="color: red">container id</span>
<span style="color: yellow">sh</span>
- docker run -it <span style="color: blue">image name</span> <span style="color: yellow">command</span>
- --

