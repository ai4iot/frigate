# How to install Docker and Docker Compose on the Raspberry PI

## Docker installation

1. Set up Docker's apt repository.
```
# Add Docker's official GPG key:
sudo apt-get update
sudo apt-get install ca-certificates curl gnupg
sudo install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/debian/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
sudo chmod a+r /etc/apt/keyrings/docker.gpg

# Add the repository to Apt sources:
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/debian \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
```

2. Install the Docker packages.
```
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

3. Verify that the installation is successful by running the hello-world image:
```
sudo docker run hello-world
```

## Install the Compose plugin

1. Update the package index, and install the latest version of Docker Compose:
```
sudo apt-get update
sudo apt-get install docker-compose-plugin
```

2. Verify that Docker Compose is installed correctly by checking the version.
```
docker compose version
```

Expected output:
```
Docker Compose version vN.N.N
```

Where is placeholder text standing in for the latest version.vN.N.N
