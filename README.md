# 90-days-devops-journey


1. What is Linux?
Linux is an open-source operating system used to run applications, servers, cloud infrastructure and containers.

For example, imagine your team develops an API.
- Developers write the API.
- QA engineers test API endpoints.
- DevOps engineers deploy the API on a Linux server.
- Users access the API through the internet.
As a QA engineer moving towards DevOps, you should be comfortable working with Linux without depending entirely on a graphical interface.
2. Set up your environment








sabbirz.com


Install these tools:
1. WSL2 – Installation guide.
2. Ubuntu – Install through Microsoft Store or WSL.
3. VS Code – Download.
Open Ubuntu terminal and execute:
sudo apt update
sudo apt upgrade -y


Verify installation:
uname -a
whoami
pwd


3. Learn these 12 essential Linux commands
Command	Purpose
pwd	Show current directory
ls	List files
ls -la	Show all files
cd	Change directory
mkdir	Create directory
touch	Create empty file
cat	Display file content
cp	Copy files
mv	Move or rename files
rm	Remove files
clear	Clear terminal
whoami	Show current user

Practical exercise
Create your first DevOps practice directory.

Execute these commands one by one:
mkdir devops-journey
cd devops-journey

mkdir linux git docker projects

touch linux/commands.txt

pwd
ls -la


Now add some content:
echo "Learning Linux for DevOps" > linux/commands.txt

cat linux/commands.txt


Copy and rename the file:
cp linux/commands.txt linux/backup.txt

mv linux/backup.txt linux/linux-notes.txt

ls linux


Expected result
Your directory structure should look like this:
devops-journey/
│
├── linux/
│   ├── commands.txt
│   └── linux-notes.txt
│
├── git/
├── docker/
└── projects/


4. Connect Linux with your QA experience
Imagine you have to test an API deployed on a Linux server.

As a QA engineer, you test:
GET /api/users
POST /api/login
PUT /api/profile


As a DevOps engineer, you should understand how to:
- Navigate application directories.
- Create configuration files.
- Manage application permissions.
- Execute scripts.
- Work with deployment directories.




# Day 2 – Linux File Permissions and Ownership

## 1. What is chmod?

`chmod` stands for **Change Mode**.

It is a Linux command used to change file or directory permissions.

It controls who can:
- Read (`r`) – View file contents.
- Write (`w`) – Modify file contents.
- Execute (`x`) – Run a file or script.

Example:

```bash
chmod +x deploy.sh
```

This adds execute permission to the deployment script.

## 2. What is chown?

`chown` stands for **Change Owner**.

It is used to change the ownership of a file or directory.

Example:

```bash
sudo chown sunil deploy.sh
```

This changes the owner of `deploy.sh` to the user `sunil`.

To change both owner and group:

```bash
sudo chown sunil:sunil deploy.sh
```

## 3. Difference between 755 and 644

Linux uses numeric values for permissions:

- Read = 4
- Write = 2
- Execute = 1

| Permission | Owner | Group | Others |
|---|---|---|---|
| 755 | Read, Write, Execute | Read, Execute | Read, Execute |
| 644 | Read, Write | Read | Read |

**755 example:**

```bash
chmod 755 deploy.sh
```

Used for executable scripts.

**644 example:**

```bash
chmod 644 notes.txt
```

Used for normal files that don't need execution permission.

## 4. How to execute a Bash script?

Step 1: Create a script.

```bash
nano deploy.sh
```

Step 2: Add the following content.

```bash
#!/bin/bash

echo "Starting deployment..."
echo "Checking application..."
echo "Deployment completed successfully!"
```

Step 3: Give execution permission.

```bash
chmod +x deploy.sh
```

Step 4: Execute the script.

```bash
./deploy.sh
```

Expected output:

```text
Starting deployment...
Checking application...
Deployment completed successfully!
```

## 5. Important interview question

**Q: What is the difference between chmod and chown?**

Answer: chmod changes file or directory permissions, whereas chown changes file or directory ownership.

## Summary

- chmod = Change permissions.
- chown = Change ownership.
- 755 = Owner has full permissions; group and others can read and execute.
- 644 = Owner can read and write; group and others can only read.
- `./deploy.sh` = Execute a Bash script from the current directory.
