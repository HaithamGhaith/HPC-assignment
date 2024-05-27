# HPC-assignment
This repo is for HPC first assignment
Dictionary Server Docker Project
Overview
This project involves creating a Docker container for a dictionary server. The server is built using a provided server.tar.gz file and runs in a containerized Ubuntu environment. The purpose is to demonstrate the use of Docker for containerizing applications, setting environment variables, and managing Docker containers.

Project Structure
Directory Setup: A dedicated directory for the project.
Dockerfile: Contains instructions to build the Docker image.
Server Archive: server.tar.gz file included in the Docker image.
Dockerfile
The Dockerfile used in this project includes the following key components:

Base Image: ubuntu:latest is used as the base image.
Environment Variables: PYTHONUNBUFFERED and PYTHONIOENCODING to handle Python output.
RUN Command: Updates and installs Python3.
ADD Command: Extracts the server.tar.gz into the root directory.
CMD Command: Specifies the command to run the server using Python.
Dockerfile
Copy code
FROM ubuntu:latest
ENV PYTHONUNBUFFERED=1
ENV PYTHONIOENCODING=UTF-8
RUN apt-get update \
 && apt-get -y upgrade \
 && apt-get -y install python3
ADD server.tar.gz /
CMD ["python3", "/server.py", "25565"]
Building the Docker Image
The Docker image is built with the following command:

sh
Copy code
sudo docker build -t dict-server:latest .
Running the Docker Container
The container is run with port mapping to allow external access to the server:

sh
Copy code
sudo docker run -d -p 42:25565 dict-server
Managing the Docker Container
List Containers: sudo docker ps -a to list all containers.
Access Logs: sudo docker logs <container_id> to view logs.
Start/Stop Container:
sh
Copy code
sudo docker stop <container_id>
sudo docker start <container_id>
Access Terminal: sudo docker exec -it <container_id> bash to access the container's terminal.
Remove Container:
sh
Copy code
sudo docker stop <container_id>
sudo docker rm <container_id>
