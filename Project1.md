
## WEB STACK IMPLEMENTATION (LAMP STACK) IN AWS
Hello, welcome to my Project1 implementation file. I will share my LAMP stack implementation with screen shots and brief notes.

I have an AWS Account set up, so I will proceed to launch a new EC2 instance of t2.micro family with Ubuntu Server 20.04 LTS (HVM).

I checked the free tier option and typed Ubuntu in the search field

![UbuntuEC2_1](https://user-images.githubusercontent.com/20802925/116267938-bf274980-a774-11eb-88d0-0ed986059684.PNG)

I selected Ubuntu Server 20.04

![UbuntuEC2_2](https://user-images.githubusercontent.com/20802925/116268159-f5fd5f80-a774-11eb-9859-d523ecbc081b.PNG)

I selected the t2.micro instance type

![UbuntuEC2_3](https://user-images.githubusercontent.com/20802925/116268755-83d94a80-a775-11eb-9e58-6b505b97fa35.PNG)

Default instance details

![UbuntuEC2_4](https://user-images.githubusercontent.com/20802925/116269069-cd299a00-a775-11eb-9447-d05c5efae873.PNG)

Default storage details

![UbuntuEC2_5](https://user-images.githubusercontent.com/20802925/116269449-22fe4200-a776-11eb-94b4-3bb399348955.PNG)

I added a tag to my instance for easy identification

![UbuntuEC2_6](https://user-images.githubusercontent.com/20802925/116269816-6e185500-a776-11eb-95e6-708900a2019c.PNG)

Default security group allowing all traffic is selected

![UbuntuEC2_7](https://user-images.githubusercontent.com/20802925/116272092-85584200-a778-11eb-8a9e-680e6b8dc493.PNG)

Review screen

![UbuntuEC2_8](https://user-images.githubusercontent.com/20802925/116272486-d9fbbd00-a778-11eb-933d-568db44a6705.PNG)

New Key Pair created and downloaded

![UbuntuEC2_9](https://user-images.githubusercontent.com/20802925/116292083-379a0480-a78d-11eb-9b31-f428ca5abfe4.PNG)

Instance launched

![UbuntuEC2_10](https://user-images.githubusercontent.com/20802925/116292345-8051bd80-a78d-11eb-9755-3a1bc16a9947.PNG)

Instance up and running

![UbuntuEC2_11](https://user-images.githubusercontent.com/20802925/116292491-ad9e6b80-a78d-11eb-9025-2036618d2028.PNG)

Connecting to my Ubuntu EC2 using  the Windows command line – Open up the command prompt

![UbuntuEC2_12](https://user-images.githubusercontent.com/20802925/116293139-72e90300-a78e-11eb-8764-d0107e7af3f9.PNG)

Copy the command to ssh into the instance - ssh -i "Lampkp.pem" ubuntu@ec2-18-218-43-122.us-east-2.compute.amazonaws.com – adjust the path to reflect the location of the key pair on your system.

![UbuntuEC2_13](https://user-images.githubusercontent.com/20802925/116293358-b5124480-a78e-11eb-872f-8e7df95d3470.PNG)

Paste the command on the command prompt

![UbuntuEC2_14](https://user-images.githubusercontent.com/20802925/116293482-dd9a3e80-a78e-11eb-82c8-c238b9a4c465.PNG)

Successfully connected to the instance

![UbuntuEC2_15](https://user-images.githubusercontent.com/20802925/116293652-07536580-a78f-11eb-9d47-5980249b4ac3.PNG)

## Step 1 — Installing Apache and Updating the Firewall

Run the sudo apt update command

![UbuntuEC2_16](https://user-images.githubusercontent.com/20802925/116294112-7cbf3600-a78f-11eb-80f4-27398839724f.PNG)

Package list updated successfully

![UbuntuEC2_17](https://user-images.githubusercontent.com/20802925/116294201-9ceef500-a78f-11eb-9976-56c6fbcb047d.PNG)

Install Apache2 server

![UbuntuEC2_18](https://user-images.githubusercontent.com/20802925/116294372-cdcf2a00-a78f-11eb-84e5-d50ab7880ea6.PNG)

Apache2 installed

![UbuntuEC2_19](https://user-images.githubusercontent.com/20802925/116294487-ee977f80-a78f-11eb-8f31-27f70da171de.PNG)

Verify Apache2 running

![UbuntuEC2_20](https://user-images.githubusercontent.com/20802925/116294632-1850a680-a790-11eb-8d73-5c9a87c3b18a.PNG)

Edit Inbound rules for security group

![UbuntuEC2_21](https://user-images.githubusercontent.com/20802925/116294857-5a79e800-a790-11eb-8eab-e0019ad648ba.PNG)

![UbuntuEC2_22](https://user-images.githubusercontent.com/20802925/116294875-5f3e9c00-a790-11eb-8cb2-6b01ef0b43cb.PNG)

Access apache server from Ubuntu shell. Server successfully accessed.

![UbuntuEC2_24](https://user-images.githubusercontent.com/20802925/116295030-8ac18680-a790-11eb-8499-692ff43caebd.PNG)

Test Apache server response to internet requests. Copy public IP address of instance and test in browser tab.

![UbuntuEC2_25](https://user-images.githubusercontent.com/20802925/116295380-ee4bb400-a790-11eb-9e28-52f6baa38808.PNG)

Web server correctly installed

![UbuntuEC2_26](https://user-images.githubusercontent.com/20802925/116295531-19360800-a791-11eb-8843-00a3ac23baf1.PNG)

## Step 2 — Installing MySQL
Run MySQL installation command

![UbuntuEC2_27](https://user-images.githubusercontent.com/20802925/116296122-bf820d80-a791-11eb-885e-124c92ee5367.PNG)

SQL installation done

![UbuntuEC2_28](https://user-images.githubusercontent.com/20802925/116296245-e4768080-a791-11eb-99ee-5e84796e3870.PNG)

Run security script $ sudo mysql_secure_installation

![UbuntuEC2_29](https://user-images.githubusercontent.com/20802925/116296505-3a4b2880-a792-11eb-9908-90c465184ca3.PNG)

![UbuntuEC2_30](https://user-images.githubusercontent.com/20802925/116296514-3ddeaf80-a792-11eb-9d67-05792fdc9ef3.PNG)

Check MySQL login. I entered a wrong command on the exit, cancelled with /c and corrected.

![UbuntuEC2_31](https://user-images.githubusercontent.com/20802925/116296782-87c79580-a792-11eb-8dae-11fd19c3a69c.PNG)

## Step 3 — Installing PHP

Run command to install multiple packages - sudo apt install php libapache2-mod-php php-mysql

![UbuntuEC2_32](https://user-images.githubusercontent.com/20802925/116297051-ce1cf480-a792-11eb-9220-974313ad457e.PNG)

![UbuntuEC2_33](https://user-images.githubusercontent.com/20802925/116297190-ec82f000-a792-11eb-9b14-7e9fa0dd214f.PNG)

Confirm PHP version installed

![UbuntuEC2_34](https://user-images.githubusercontent.com/20802925/116297308-0c1a1880-a793-11eb-8e00-391091d32801.PNG)

## Step 4 — Creating a Virtual Host for your Website using Apache

Create directory for projectlamp & assign ownership of the directory

![UbuntuEC2_35](https://user-images.githubusercontent.com/20802925/116297643-62875700-a793-11eb-9f1d-afac4e8a4ba1.PNG)

Create and open configuration file. Modify the file, paste in the configuration text.

![UbuntuEC2_36](https://user-images.githubusercontent.com/20802925/116297826-995d6d00-a793-11eb-94cb-1cb29ee4bc7b.PNG)

Enable the new virtual host. Disable Apache's default website. Check configuration file for syntax errors. Reload apache2

![UbuntuEC2_37](https://user-images.githubusercontent.com/20802925/116298506-6c5d8a00-a794-11eb-8c28-44d553c03647.PNG)

Create index.html file

![UbuntuEC2_38](https://user-images.githubusercontent.com/20802925/116298767-c78f7c80-a794-11eb-9cbf-37d8c93aa3c6.PNG)

Open website url using IP address

![UbuntuEC2_39](https://user-images.githubusercontent.com/20802925/116298910-f4dc2a80-a794-11eb-82fb-ea07aa4aecee.PNG)

Open website url using domain name

![UbuntuEC2_40](https://user-images.githubusercontent.com/20802925/116299031-16d5ad00-a795-11eb-98fe-c9bea131d432.PNG)

## Step 5 — Enable PHP on the website
Run commands to edit the dir.conf file, reload Apache2 and create a new index.php file. 

![UbuntuEC2_41](https://user-images.githubusercontent.com/20802925/116299195-48e70f00-a795-11eb-9774-c4c10c6a8b56.PNG)

![UbuntuEC2_42](https://user-images.githubusercontent.com/20802925/116299638-d75b9080-a795-11eb-9472-fbc16240968e.PNG)

Refresh your web browser tab

![UbuntuEC2_43](https://user-images.githubusercontent.com/20802925/116299769-0540d500-a796-11eb-8204-dd52b9395159.PNG)

Remove the index.php file

![UbuntuEC2_44](https://user-images.githubusercontent.com/20802925/116300065-594bb980-a796-11eb-834e-b1cffcc2870e.PNG)

Project completed. Thank you.
