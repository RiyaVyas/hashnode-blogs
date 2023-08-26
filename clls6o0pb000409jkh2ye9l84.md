---
title: "📝 Demystifying File Permissions and Access Control Lists (ACLs) 📝"
seoTitle: "Linux File Permissions"
seoDescription: "Demystifying File Permissions and Access Control Lists (ACLs)"
datePublished: Sat Aug 26 2023 15:35:26 GMT+0000 (Coordinated Universal Time)
cuid: clls6o0pb000409jkh2ye9l84
slug: demystifying-file-permissions-and-access-control-lists-acls
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1693063987037/171e30a0-aab7-4f1f-869f-accb7e77565d.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1693064062135/c576cfa0-1817-48b4-aeda-e4139b2c5fd6.png
tags: devops, linux-for-beginners, 90daysofdevops, day6, linux-file-permissions

---

## Introduction:

Hey there, tech enthusiasts! 👋 Have you ever wondered how your computer decides who can access your files and who can't? 🤔 Well, fret not! 🛡️ In this blog, we're going to unravel the mysteries of file permissions and take a peek into the fascinating realm of Access Control Lists (ACLs). 🕵️‍♂️

## Part 1: Understanding File Permissions 📝🔑

Imagine your files as treasure chests 🏴‍☠️ – you wouldn't want just anyone to be able to open them, right? That's where file permissions come into play. They're like the locks on these virtual chests, ensuring that only authorized users can access your precious data.

In the linux world, you must have seen commands like 'ls -lrth' that display something like this -

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693063234531/36f8c2ba-4602-4e31-809e-ff0fb7ff5d22.png align="center")

Those letters and hyphens represent the file's permission mode for different user groups. Lets understand this in detail.

**1\. Who's Who in Permissions:** File permissions revolve around three main roles:

👤 **Owner:** The creator of the file. They have the highest level of control.

👥 **Group:** A collection of users with shared permissions.

🌍 **Others:** Everyone else who's not the owner or in the group.

**2\. Permission Types:** Files can have three basic permissions:

📖 **r:** **Read:** Allows viewing the contents of a file.

✏️ **w: Write:** Permits making changes to a file.

🚫 **x: Execute:** Enables running scripts or programs.

In the above example, -rwxrwxrwx means, the owner, its group and all others can read, write and execute the file.

## 🤝 Taking Control with ACLs 🤝

Access Control Lists (ACLs) add an extra layer of finesse to file permissions. They allow you to define specific access rules for individual users and groups. It's like having different keys to open various compartments within the treasure chest! 🔐

### 📝 Try It Out! `getfacl` and `setfacl`

Let's get hands-on! Meet `getfacl` and `setfacl`—two command-line superheroes that help us manage ACLs. Imagine you have a directory named `project_docs`, and you want your team members to have different levels of access:

1. Alice should be able to read, write, and execute.
    
2. Bob can read and write, but not execute.
    
3. Carol has read-only access.
    

Here's how you'd do it using `setfacl`:

```powershell
# Give Alice full access
setfacl -m u:alice:rwx project_docs

# Give Bob read and write access
setfacl -m u:bob:rw- project_docs

# Give Carol read-only access
setfacl -m u:carol:r-- project_docs
```

To view the ACLs, use `getfacl` :

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693063769999/91c0a8b2-a204-441c-9942-9911d3e65575.png align="center")

## 🚀 Conclusion 🚀

Congratulations! 🥳 You've just gained a superpower in the realm of file permissions and ACLs. Now you can confidently control who accesses your digital treasures and who gets to modify or execute them. Remember, this knowledge comes with great responsibility—use it wisely! 🌟 So go ahead, venture into your terminal, and become the master of your files. 🛡️🔒

That wraps up our journey into the world of file permissions and ACLs. We hope you found this adventure enlightening and empowering. Until next time, stay curious and keep exploring! 🌐🔍