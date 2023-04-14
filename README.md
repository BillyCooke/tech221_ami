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
