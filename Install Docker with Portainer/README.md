How to Install Docker and Portainer on a Linux Machine

This guide will walk you through installing Docker on a Linux machine and setting up Portainer as a container management interface.

Prerequisites

A Linux machine with root or sudo access

Internet connection

# Step 1: Update the System

Before installing Docker, make sure your system is up-to-date.

```bash
sudo apt update
sudo apt upgrade -y
```

Step 2: Install Required Dependencies

Install packages required for Docker installation.

```bash
sudo apt install apt-transport-https ca-certificates curl software-properties-common -y
```

Step 3: Add Docker's Official GPG Key and Repository

```bash
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
sudo add-apt-repository "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
```

Step 4: Install Docker

Update the package index and install Docker.

```bash
sudo apt update
sudo apt install docker-ce -y
```

Step 5: Start and Enable Docker Service

```bash
sudo systemctl start docker
sudo systemctl enable docker
```

Step 6: Verify Docker Installation

Check Docker version to ensure it's installed correctly.

```bash
docker --version
```

You can also run a test container:

```bash
sudo docker run hello-world
```

Step 7: Install Portainer

Portainer is a lightweight management UI for Docker.

7.1 Create a Docker Volume for Portainer

```bash
sudo docker volume create portainer_data
```

7.2 Run the Portainer Container

```bash
sudo docker run -d -p 8000:8000 -p 9000:9000 --name=portainer --restart=always \
-v /var/run/docker.sock:/var/run/docker.sock \
-v portainer_data:/data \
portainer/portainer-ce
```

7.3 Access Portainer UI

Open a web browser and navigate to:

http://<your-server-ip>:9000

Create an admin user and set up your Docker environment.

Step 8: Enable Docker to Run Without Sudo (Optional)

If you want to run Docker without sudo, add your user to the Docker group.

```bash
sudo usermod -aG docker $USER
newgrp docker
```

Conclusion

## You have successfully installed Docker and set up Portainer on your Linux machine. You can now manage your Docker containers through the Portainer web UI.
