### DOCKER
### Install Docker and Docker Compose on your OS using next command step by step:

## 1. Install main tools

    sudo apt-get install -y \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
    software-properties-common

## 2. Download gpg-key

    curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

## 3. Add docker repository
    sudo add-apt-repository \
    "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
    $(lsb_release -cs) \
    stable"
## 4. Update packages

    sudo apt-get update -y

## 5. Install docker.io
    sudo apt-get install -y docker-ce docker-ce-cli containerd.io

#### Postinstal settings ...

## 7. Add user
    sudo usermod -aG docker $USER
## 8. Enable user
    newgrp docker
## 9. Test
    docker run hello-world
## 10. Enable docker on start system
    sudo systemctl enable docker

## 11. Install docker compose
    sudo curl -L "https://github.com/docker/compose/releases/download/1.25.4/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
## 12. add permissions for docker compose
    sudo chmod +x /usr/local/bin/docker-compose
