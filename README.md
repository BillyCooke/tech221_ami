# Creating an instance with an AMI

## What is an AMI?
An AMI is an Amazon Machine image that contains software configuration and from this you can launch instances.

## We can create an AMI using a previously made instance by following the steps below
* Select your running instance and click the actions drop down at the top of the page and then select image and templates
* Then select create an image which will take you to the page to create an AMI
* You will need to create a name for the AMI which will need to be easily identifiable for you in the future
* You can also add a description if you would like again to help you in the future
* That's all we need to do for this so then click create an image

## To launch a new instance from this AMI
* Go into the dashboard on the left and select AMI's
* Search in your name or what you saved the AMI as
* Select the AMI and click the launch instance from AMI button at the top of the page
* This will bring you to the normal launch instance page
* Name your instance and scroll down to AMI
* The AMI has already been selected for us and you can see this by looking at the name you created for it
* Scroll down again to key pair and search tech221
* Then add your previously made security group by searching your name
* Then launch the instance
* To make sure the instance is working with Nginx you can go to your instance and copy the public IP address and paste it into a new browser which will bring up "Welcome to Nginx"

## Diagram of an AMI
The diagram below shows the interactions with an AMI to instances. You can create one or multiple instances from a single AMI.

![img.png](img.png)

## You can add Nginx in AWS without using Git Bash
* When you are setting up an instance follow all the normal steps
* In additional details scroll to the bottom to user data
* In user data enter the script below
```* #!/bin/bash
* sudo apt update -y
* sudo apt update -y
* sudo apt install nginx -y
* sudo systemctl restart nginx
* sudo systemctl enable nginx
```
* Then launch the instance as normal

## Variables in Linux
* When you are linked into AWS via SSH on Git Bash follow the below
* To see the list of environment variables already listed use ```printenv``` or ```env```
* To see a specific variable use ```printenv 'name of variable'```. If nothing comes up then the variable does not exist
* To create a variable use ```'name of variable'='data'```. For example ```MY_NAME=billy``` created the variable MY_NAME and assigns it the value billy
* To see a variable use ```echo $'name of variable'```. Example ```echo $MY_NAME``` will bring up billy
* To create an environment variable use ```export 'name of variable'='data'```. Example ```export LAST_NAME=cooke```
* To see the environment variable in the list use ```printenv``` or ```env```
* To see the environment variable on its own use ```printenv 'name of variable```
* If you come out of the Linux environment in Git Bash none of the above will save
* To save a variable permanently use the below
* Enter ```sudo nano .bashrc``` and this will bring up all the persistent variables
* Scroll to the bottom and type ```export 'name of variable'='data'```. Example ```export name=billy```
* Then use ```ctrl s``` to save and ```ctrl x``` to exit
* To view the .bashrc file use ```cat .bashrc```
* To refresh .bashrc to implement the changes you have made use ```source .bashrc```
* To check it has worked use ```printenv 'name of variable``` and it should show the persistent variable you have made

## To view the permissions on a file
* ```ls -l```

## Setting permissions in Linux
* 'r' is for read
* 'w' is for write
* 'x' is for execute
* chmod +rwx 'filename' to add permissions
* chmod -rwx 'filename' to remove permissions
* chmod +x 'filename' to allow executable permissions
* chmod 'filename' to take out write and executable permissions
