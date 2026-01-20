# Updating and Installing the package after Setting it up



```bash
sudo apt update .
```
Update the package list in the server to there latest version 

```bash
sudo apt install <package>  
```
Install the specific package  

```bash
sudo apt upgrade  
```
Upgrades all the installed package to there latest version 

------------------------------------------------------------------------------------------------------------------------------------------------- 

# Installation of Jenkins 

```bash
  sudo apt install -y open jdk-17-jdk
```
```bash
curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key | sudo tee \
  /usr/share/keyrings/jenkins-keyring.asc > /dev/null
```
```bashecho deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
```
```bash
sudo apt update
sudo apt install -y jenkins
sudo systemctl start jenkins
```

# Give Jenkins access to the Docker 

```bash
sudo usermod -aG docker jenkins
sudo systemctl restart jenkins
```
# Access the Jenkins at 

```bash
http://<VM-IP>:8080
```

---------------------------------------------------------------------------------------------------------------------------------------------

# Docker Installation 

```bash
sudo apt update
sudo apt install -y docker.io
sudo systemctl enable docker
sudo systemctl start docker
```

# Add the your current user to the gruop 
```bash
sudo usermod -aG docker $USER
newgrp docker
```

# To  Verify the installation 

```bash
docker run hello-world
```


