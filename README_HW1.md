# CNS Homework 1
#### Alexander Mathes
#### Computer Network Security
#### 30AUG23
## Automate Webserver Creation
For this tutorial we are going to be learning how to provision a virtual machine automatically so that you would not need to manually install your webserver every time you boot up your machine.  The prerequisites for this is to have the latest version of Vagrant and have a visualization product downloaded.  We will be using VirtualBox.
##### Create an HTML directory
First we need to create a new directory for our html file and it will simply be named html.  Afterward we need to create our html file which will house the content of the website.  In the tutortial it says to make index.html, but for the purposes of this homework, we will be using Homework_1.html.
![Screenshot showing the html directory and Homework_1.html file, as well as its contents.](https://github.com/RoboTurtle/CNS/assets/70544712/0ac19274-221e-409c-80ae-854b0f566274)

##### Write a provisioning script
After we set up our HTML file, we need to make a provisioning script.  We create a file called bootstrap.sh in the same directory as our Vagrantfile and insert the provided code.
![Screenshot showing bootstrap.sh and its contents.](https://github.com/RoboTurtle/CNS/assets/70544712/0ac768d0-18dd-41c7-9a4d-57c13e52cd96)

##### Configure Vagrant
In our Vagrantfile file, we added the line config.vm.provision :shell, path: "bootstrap.sh" in order to use the script after it is provisioned.
##### Deploying the webserver and verifying deployment
We use the vagrant up command to create and automatically provision our machine and then we verify that the provisioning worked by loading a file from within the machine.
![Screenshot showing that the provisioning worked.](https://github.com/RoboTurtle/CNS/assets/70544712/1e1b798a-4a43-475a-afe2-a5ddff15784b)

## Configure Network
For this tutorial, we will be using avaliable networking features in order to access the website hosted from the guest machine on the host machine.  
The prerequisites for this will be that the previous tutorial was completed.
##### Configure port forwarding
With port forwarding, it will allow us to specify ports on the guest machine so that we can share it with our host machine.  This would allow us to access the port on the guest machine directly from our host machine without the need to ssh into the guest machine.  In order to do this we must add a config.wm.network line to our code in the Vagrantfile file.
![Screenshot showing the added config.wm.network line of code.](https://github.com/RoboTurtle/CNS/assets/70544712/65817dfa-f28b-4372-b957-32723e33bcfd)
##### Access the served files
Now we can be on our host machine and go to 127.0.0.1:4567 and access our webserver.
![Screenshot showing the initial index of the website.](https://github.com/RoboTurtle/CNS/assets/70544712/340aae61-b569-4140-8be9-996d0026389c)
![Screenshot showing the contents of the Homework_1.html file on the website](https://github.com/RoboTurtle/CNS/assets/70544712/ea024ca9-3de5-4d49-9fd9-b0d9302accbe)





