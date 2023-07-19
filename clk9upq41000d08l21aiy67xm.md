---
title: "Unveiling the Power of Shell Scripting in DevOps: Harnessing the Kernel's Secrets"
seoTitle: "Unveiling the Power of Shell Scripting in DevOps"
seoDescription: "Unveiling the Power of Shell Scripting in DevOps: Harnessing the Kernel's Secrets"
datePublished: Wed Jul 19 2023 15:01:17 GMT+0000 (Coordinated Universal Time)
cuid: clk9upq41000d08l21aiy67xm
slug: unveiling-the-power-of-shell-scripting-in-devops-harnessing-the-kernels-secrets
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1689778781511/4b8a23e6-9841-4745-bb39-6df8b8516cab.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1689778818505/ecf18f3a-62cd-4ebb-99cb-c58ce524c383.png
tags: devops, shell-scripting, 90daysofdevops, day4, trainwithshubham

---

# 🌽 What is a Kernel? 🌽

The kernel is like the core of an operating system. It's the part that interacts directly with the hardware and manages system resources. Think of it as the master conductor of an orchestra, ensuring that all the different parts of the system work harmoniously together.

# 🐚 What is a Shell? 🐚

A shell is like a command-line interpreter that acts as a user interface to interact with the kernel. It's like a shell of a nut, protecting and providing access to the precious kernel inside. The shell takes your commands, passes them to the kernel, and displays the results back to you.

# 📜 What is Shell Scripting for DevOps? 📜

Shell scripting is the art of writing scripts (series of commands) that can be executed by a shell. In the context of DevOps, it refers to using shell scripts to automate tasks and streamline processes in the world of software development and IT operations. It's like having a reliable assistant that can perform repetitive tasks for you.

To put it simply, think of these as the following -

# 💡 Real-Life Analogies 💡

## 🌐 **Kernel**:

Imagine the kernel as the CEO of a company. It handles the low-level operations and resources, ensuring everything runs smoothly behind the scenes.

## 💬 **Shell**:

Think of the shell as the receptionist at the front desk. It takes your requests, passes them to the appropriate department, and relays the responses back to you.

## 🤖 **Shell Scripting**:

Visualize shell scripting as a personal assistant. It follows your instructions, performs tasks on your behalf, and frees up your time for more important things.

# 🙋Questions at hand

1. ## What is #!/bin/bash? can we write #!/bin/sh as well?
    

The shebang line, often written as "#!/bin/bash" or "#!/bin/sh", is a special directive found at the beginning of a shell script file. It specifies the interpreter or shell that should be used to execute the script.

* **#!/bin/bash**: This shebang line indicates that the script should be interpreted using the Bash shell. Bash (Bourne Again SHell) is a widely used and powerful shell that provides additional features and functionalities compared to the standard Bourne shell.
    
* **#!/bin/sh**: This shebang line specifies the use of the default system shell, which may or may not be Bash. In many Unix-like systems, `/bin/sh` is a symbolic link to the system's preferred shell. It's typically a compatible shell, such as Bash, Dash, or another variant of the Bourne shell.
    

So yes, we can use either "#!/bin/bash" or "#!/bin/sh" in our script.

However, keep in mind that if you choose "**#!/bin/bash**", you're explicitly requesting the **Bash shell**, which may not be available on all systems. On the other hand, "**#!/bin/sh**" allows for greater portability, as it will use the **default system shell**.

To find the default shell in our system, we can use the $SHELL command.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689776781960/d526d4d0-56c9-4f89-9cc6-f5d696297d7f.png align="center")

1. ## Write a Shell Script which prints I will complete #90DaysOofDevOps challenge.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689777147027/9d88f295-08c6-46e8-a616-47ab64a12825.png align="center")

1. ## Write a Shell Script to take user input, input from arguments and print the variables.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689777804482/244aa378-06f2-43c0-9654-0d49e7e6ba92.png align="center")

1. Write an Example of If else in Shell Scripting by comparing 2 numbers.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689778669872/6b8fdfb2-0e5b-4e0c-b11a-a46d402775e7.png align="center")

We have thus demonstrated some basic shell scripting skills.

This concludes the blog for #day4.