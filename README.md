# jenkinstrigger

#Task: Deployment Automation ChallengeObjective: Automate the deployment of a sample web application using a tool of your choice.

Dear Sir/Madam,

Hi have used AWS EC2 instance for installing jenkins on that server.
I have refer jenkins docs for installing. below are the commands that are use for installing jenkins.

sudo apt update

sudo apt install openjdk-11-jdk -y

sudo wget -O /usr/share/keyrings/jenkins-keyring.asc \
  https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key

echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null

sudo apt-get update

sudo apt-get install jenkins -y

#Choose a simple web application (e.g., a "Hello World" app). Select a deployment tool (e.g., Ansible, Bash scripts) that you are comfortable with.

I have used https://www.tooplate.com/free-templates for sample website.


#Create an automation script that accomplishes the following: Downloads and sets up the required dependencies for the web application.

For continuos deployment i'm using Github Actions for the same. so once we push the changes to the repository it will fetch the latest chnage and jenins will build the job and run.

#Steps

1. Created AWS EC2 Instance and choose ubuntu AMI and created security group and key pair for the same.
2. After staring the instance i have installed jenkins on that instance.
3. once jenkins is installed than we can use jenkins on localhost.
4. so in jenkins i have created pipeline and chooses github version control for the code
5. i have created git repo for stroting the and version control
6. once the sample website is pushed to git repo is done
7. i have added git webhook to connect with jenkins server.
8. and after that if we push any changes to repo than jenkins will automatically fetch that repo and build the job.
