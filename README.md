This repo is for HPC first assignment
# Dictionary Server Docker Project

## Overview

This project involves creating a Docker container for a dictionary server. The server is built using a provided `server.tar.gz` file and runs in a containerized Ubuntu environment. The purpose is to demonstrate the use of Docker for containerizing applications, setting environment variables, and managing Docker containers.

## Project Structure

- **Directory Setup**: A dedicated directory for the project.
- **Dockerfile**: Contains instructions to build the Docker image.
- **Server Archive**: `server.tar.gz` file included in the Docker image.

## Dockerfile

The Dockerfile used in this project includes the following key components:

- **Base Image**: `ubuntu:latest` is used as the base image.
- **Environment Variables**: `PYTHONUNBUFFERED` and `PYTHONIOENCODING` to handle Python output.
- **RUN Command**: Updates and installs Python3.
- **ADD Command**: Extracts the `server.tar.gz` into the root directory.
- **CMD Command**: Specifies the command to run the server using Python.

## Building the Docker Image

The Docker image is built with the following command:


## Screenshots

Below are key screenshots demonstrating the process:

1. **Docker Installation**: After installing Docker.
2. **Project Directory**: Directory structure with `server.tar.gz`.
3. **Dockerfile Creation**: Content of the Dockerfile.
4. **Building Image**: Output of the build process.
5. **Running Container**: Container running in detached mode.
6. **Listing Containers**: Output of `sudo docker ps -a`.
7. **Accessing Logs**: Logs from the running container.
8. **Start/Stop Container**: Status changes of the container.
9. **Terminal Access**: Inside the container's terminal.
10. **Removing Container**: Confirming container removal.

## Conclusion

This project demonstrates the process of containerizing a Python-based dictionary server using Docker, managing containers, and handling basic Docker commands to build, run, and maintain the containerized application.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.


