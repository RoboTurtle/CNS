# CNS Homework 1
#### Alexander Mathes
#### Computer Network Security
#### 30AUG23
## Automate Webserver Creation
For this tutorial we are going to be learning how to provision a virtual machine automatically so that you would not need to manually install your webserver every time you boot up your machine.  The prerequisites for this is to have the latest version of Vagrant and have a visualization product downloaded.  We will be using VirtualBox.
##### Create an HTML directory
First we need to create a new directory for our html file and it will simply be named html.  Afterward we need to create our html file which will house the content of the website.  In the tutortial it says to make index.html, but for the purposes of this homework, we will be using Homework_1.html.
![Screenshot showing the html directory and Homework_1.html file, as well as its contents.](<img width="514" alt="html_ss" src="https://github.com/RoboTurtle/CNS/assets/70544712/8b41cebb-bf36-4ba0-be4f-0c489faa79f5">)
##### Write a provisioning script
After we set up our HTML file, we need to make a provisioning script.  We create a file called bootstrap.sh in the same directory as our Vagrantfile and insert the provided code.
![Screenshot showing bootstrap.sh and its contents.](<img width="650" alt="bootstrapss" src="https://github.com/RoboTurtle/CNS/assets/70544712/fcc44b06-f7ad-4eab-ad98-e33f39c7fb90">)



