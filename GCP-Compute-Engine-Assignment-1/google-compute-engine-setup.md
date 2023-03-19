# Setting up a Google Compute Engine with Nginx
### _In this assignment, I created a Google Compute Engine instance with Debian GNU/Linux 11 (bullseye) as the boot disk image, installed and configured Nginx web server using a startup script, reserved an external IP address, and captured an image of the Nginx webpage. Below are the step-by-step instructions to recreate this setup._


- Prerequisites
 _Before starting, you will need to have a Google Cloud Platform account and a project set up. You should also have basic knowledge of the Google Cloud Platform console and how to create and manage Compute Engine instances._



## Steps
1.***Open the Google Cloud Platform console and navigate to the Compute Engine section.***	
2.***Click on the "Create" button to create a new instance.***	
3.***Choose a name for your instance and select "e2-micro" as the machine type.***	
4.***In the "Boot disk" section, choose "Debian GNU/Linux 11 (bullseye)" as the boot disk image.***	
5.***In the "Firewall" section, allow HTTP traffic so that the Nginx server can be accessed from the internet.***	
6.***In the "Management, security, disks, networking, sole tenancy" section, choose a network and subnet based on your preference or the ones you created in a previous session.***	
7.***In the "Cloud API access scopes" section, choose "Allow default access".***
8.***In the "Metadata" section, add a startup script to install Nginx. Copy and paste the following script:***

```
sudo apt-get update
sudo apt install nginx -y
```
9.***Click "Create" to create the instance.***	
10.***Wait for the instance to be created and for the startup script to finish running.***	
11.***Once the instance is running, click on the external IP address to see the default Nginx web page.***	
12.***To reserve the external IP address, click on the "Reserve" button next to the IP address.***	13.***Choose a name for the reservation and click "Reserve".***


### Done :) now you can use this setup to serve your own web pages on the internet