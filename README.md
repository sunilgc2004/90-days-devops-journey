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
