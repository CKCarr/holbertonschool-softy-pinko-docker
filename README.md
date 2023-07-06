##Docker
# holbertonschool-softy-pinko-docker

 **Task 0**
 "This Dockerfile is for Task 0, which is aimed at creating a basic Docker image. The image is based on the latest Ubuntu version available. Here's a breakdown of the Dockerfile's instructions:

FROM docker.io/library/ubuntu:latest: This line specifies the base image for our Docker image, which is the latest version of Ubuntu available from the official Docker registry.

RUN apt-get update: This instruction updates the package lists for Ubuntu to ensure we have the latest information about available packages.

RUN apt-get upgrade -y: This instruction upgrades the currently installed software on the Ubuntu image to the latest versions. The -y flag is used to automatically answer 'yes' to any prompts that might appear during the upgrade process.

CMD echo "Hello, World!": The CMD instruction sets the default command to be executed when a container based on this image is run. In this case, it echoes the "Hello, World!" message to the terminal.

To build and run the Docker image, you would navigate to the directory containing the Dockerfile and execute the following commands:

docker build -f ./Dockerfile -t softy-pinko:task0 .: This command builds the Docker image based on the Dockerfile and tags it with the name softy-pinko and the tag task0.
docker run -it --rm --name softy-pinko-task0 softy-pinko:task0: This command runs a container based on the softy-pinko:task0 image, allowing you to interact with the "Hello, World!" message.
Overall, this Dockerfile sets up a basic Ubuntu-based image, updates and upgrades the system software, and defines a default command that displays a simple message. It serves as a starting point for further customization and development of Docker images and containers."

 **Task 1**
 This Dockerfile sets up a Docker image that includes an Ubuntu base. It installs Python3, pip3, and Flask, and then copies the api.py file, which contains a simple Flask server code. When a container is created from this image, it runs the Flask server, allowing it to respond to requests on a specific port. This setup allows us to easily deploy and run the Flask server in a Docker container, providing a scalable and isolated environment for our application.
