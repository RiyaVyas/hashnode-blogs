---
title: "A Beginner's Guide to Package Managers, Docker, and Jenkins on Ubuntu"
seoTitle: "Understanding Package Managers on Ubuntu"
seoDescription: "A Beginner's Guide to Package Managers, Docker, and Jenkins on Ubuntu"
datePublished: Sat Aug 26 2023 17:19:13 GMT+0000 (Coordinated Universal Time)
cuid: cllsadhgo000709lj6yho9cgj
slug: a-beginners-guide-to-package-managers-docker-and-jenkins-on-ubuntu
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1693069540268/62e791e3-a8f1-4ba9-a1db-d127f113aa0d.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1693069692944/ee4bc368-9f6f-4d6a-9fdb-79d161863502.jpeg
tags: linux, devops, package-manager, 90daysofdevops, day7

---

# 📦 **Understanding Package Managers on Ubuntu** 📦

Package managers are like digital shopping assistants for your computer. They simplify the process of installing, updating, and managing software on your system. Think of them as app stores for your operating system, allowing you to easily find and install various programs and libraries. On Ubuntu, a popular Linux distribution, two commonly used package managers are **APT** (Advanced Package Tool) and **DPKG**.

**APT**: This is your primary tool for managing packages. It's responsible for fetching packages from online repositories and installing them with all their dependencies.

**DPKG**: This works at a lower level and is used to install individual Debian package files. APT actually uses DPKG in the background.

Now that we've got the basics, let's dive into how to use package managers to install two important tools: **Docker** and **Jenkins**.

## 🐳 **Installing Docker on Ubuntu Using Package Managers** 🐳

Docker allows you to put applications and their dependencies into containers for consistent and reliable deployment. Here's how to get started:

1. **Open Your Terminal**: Launch the terminal on your Ubuntu system.
    
2. **Update Package List**: Run the following command to ensure you have the latest package information:
    
    ```powershell
    sudo apt update
    ```
    
3. **Install Docker's Dependencies:** You need a few things before you can install docker. Get them by running:
    
    ```powershell
    sudo apt install apt-transport-https ca-certificates curl software-properties-common
    ```
    
4. **Add Docker Repository:** This adds the official docker repository to your system:
    
    ```powershell
    curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
    echo "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
    ```
    
5. **Install Docker Engine:** Update your system and now install docker using apt package manager.
    
    ```powershell
    sudo apt update
    sudo apt install docker-ce docker-ce-cli containerd.io
    ```
    
6. **Start and Enable Docker:** These commands ensure Docker starts on boot:
    
    ```powershell
    sudo systemctl start docker
    sudo systemctl enable docker
    ```
    
7. **Verify Installation:** Check if Docker is installed and running.
    
    ```powershell
     docker --version
    ```
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693065956624/5a6a062e-9ca4-4b3d-9f49-ee1ad3ea9ff3.png align="center")

🤖**Setting Up Jenkins on Ubuntu Using Package Managers** 🤖

Jenkins is an automation tool that makes building, testing, and deploying software easier. Let's get it up and running:

1. **Update/Install JDK on your system**
    

```powershell
sudo apt update
sudo apt install openjdk-17-jre
java -version
```

1. **Update Package List**: Update your package list to include the Jenkins repository:
    
    ```powershell
    sudo apt update
    ```
    
2. **Install Jenkins:** Now install jenkins using APT package manager.
    
    ```powershell
    curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key | sudo tee \
      /usr/share/keyrings/jenkins-keyring.asc > /dev/null
    echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
      https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
      /etc/apt/sources.list.d/jenkins.list > /dev/null
    sudo apt-get update
    sudo apt-get install jenkins
    ```
    
3. **Start and Enable Jenkins:** Start the jenkins service and set it to start on boot.
    
    ```powershell
    sudo systemctl start jenkins
    sudo systemctl enable jenkins
    ```
    
4. **Get initial Admin Password:** Retrieve the initial admin password to complete setup.
    
    ```powershell
    sudo cat /var/lib/jenkins/secrets/initialAdminPassword
    ```
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693069454964/5ef87068-5f3a-4c39-bf0e-21adfc48c5f1.png align="center")

# 🎉 **Conclusion** 🎉

Congratulations! You've just installed Docker and Jenkins on your Ubuntu system using package managers. 🎈 Package managers simplify software management, making it as easy as adding items to your online shopping cart. Docker containers and Jenkins automation are powerful tools that can greatly enhance your development workflow. Now you're equipped with the ability to seamlessly manage and deploy software. Remember, these tools are essential in the modern world of software development, and understanding how to use them will make your life much easier. Happy coding! 😄🚀