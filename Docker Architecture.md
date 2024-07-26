# **Docker Architecture**

![image](https://github.com/user-attachments/assets/49884dd3-f233-4ea7-8896-117eb93c0575)

### Docker Client 
This is an application which is part of the docker engine which is responsible for accepting docker commands from the user and passing it to docker daemon.
### Docker Host 
The machine on which docker is installed is called docker host. It can be Windows, Linux or Mac.
### Docker Daemon 
This is the background process which is also part of the docker engine. Responsibility of docker daemon is to accept the commands from the docker client and perform necessary action.
### Docker Registry
The place where we store docker images is docker registry. These are two types:
 1) Public Docker Registry.
 2) Private Docker Registry. 
Public docker Registry is the hub.docker.com images uploaded here will be accessed by anyone. Private docker registry is private to a particular organization or particular team. Only they can access the images in these registries.

![image](https://github.com/user-attachments/assets/139adb5a-f53f-4d5d-bc8b-ea29f2abd479)

## Architecture Steps
* Step1: When we execute the command from the docker client (i.e. docker pull nginx).
            This command will be listened to by docker daemon.
* Step2: Docker daemon will be connecting to the docker registry and find the Nginx image 
           in docker registry & perform action.
* Step3: Now this Docker daemon will be downloading nginx image from docker registry.
* Step 4: In docker client we have to executed a command to run a container 
            (docker run–name=app-d-p 8080:8080 nginx) that will be listened to by docker daemon.
* Step 5: Docker daemon will check nginx image is available or not in docker host if image available
             it will not go to the docker Registry.
* Step 6: docker daemon will take downloaded image and run the application 


















 


             
