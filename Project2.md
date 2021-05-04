## WEB STACK IMPLEMENTATION (LEMP STACK)

Hello, welcome to my Project2 implementation file. I will share my LEMP stack implementation with screen shots and brief notes.

I set up my EC2 Instance of t2.micro family with Ubuntu Server 20.04 LTS (HVM) image.

![Proj2_1](https://user-images.githubusercontent.com/20802925/116990120-96e6a000-acca-11eb-8639-454aee118d1e.PNG)

I lauched Git Bash and navigated to my keypair folder. I then executed the ssh command into my instance.

![Proj2_2](https://user-images.githubusercontent.com/20802925/116990388-f2b12900-acca-11eb-904d-ebf0d23f642e.PNG)

I executed the sudo apt update command followed by the nginx installation command.

![Proj2_3](https://user-images.githubusercontent.com/20802925/116990632-4f144880-accb-11eb-93b6-ee7c623e9272.PNG)

![Proj2_4](https://user-images.githubusercontent.com/20802925/116990641-52a7cf80-accb-11eb-878e-dc2c04c4966a.PNG)

![Proj2_5](https://user-images.githubusercontent.com/20802925/116990660-563b5680-accb-11eb-8641-4cfd222f4c32.PNG)

![Proj2_6](https://user-images.githubusercontent.com/20802925/116990670-59364700-accb-11eb-9082-ab9e4fc0ce14.PNG)

I verified the successful installation of the nginx web server with the sudo systemctl status nginx command

![Proj2_7](https://user-images.githubusercontent.com/20802925/116990930-b7fbc080-accb-11eb-9635-5e396ceab1d2.PNG)

I modified the instance security group to open an inbound connection through port 80.

![Proj2_8](https://user-images.githubusercontent.com/20802925/116991110-f8f3d500-accb-11eb-9e1c-9afa115f30e9.PNG)

I accessed the server locally through the ubuntu shell

![Proj2_9](https://user-images.githubusercontent.com/20802925/116991266-35273580-accc-11eb-880c-42d3fafdf68c.PNG)

Then I tested the nginx server response via the internet.

![Proj2_10](https://user-images.githubusercontent.com/20802925/116991521-92bb8200-accc-11eb-9840-9633a29e7bb3.PNG)

## Step 2 — Installing MySQL

I then proceeded to install MySQL

![Proj2_11](https://user-images.githubusercontent.com/20802925/116991645-c8606b00-accc-11eb-85ec-38a9dfd6df45.PNG)

![Proj2_12](https://user-images.githubusercontent.com/20802925/116991691-dca46800-accc-11eb-939a-f1e79714a889.PNG)

I ran the security script provided.

![Proj2_13](https://user-images.githubusercontent.com/20802925/116991986-47ee3a00-accd-11eb-9a6a-e05c0715d165.PNG)

![Proj2_14](https://user-images.githubusercontent.com/20802925/116991997-4ae92a80-accd-11eb-882d-3fab0c40d239.PNG)

![Proj2_15](https://user-images.githubusercontent.com/20802925/116992006-4d4b8480-accd-11eb-9e6b-d2b1050f0306.PNG)

![Proj2_16](https://user-images.githubusercontent.com/20802925/116992014-50467500-accd-11eb-811b-c63c331e2b7e.PNG)

I then ran the sudo mysql command to test log in.

![Proj2_17](https://user-images.githubusercontent.com/20802925/116992386-d4006180-accd-11eb-9c0c-ccccbd84ed96.PNG)

## Step 3 – Installing PHP

I proceeded to install PHP with the command provided, sudo apt install php-fpm php-mysql.

![Proj2_18](https://user-images.githubusercontent.com/20802925/116993086-e333df00-acce-11eb-8604-ea1dfe2c3d94.PNG)

![Proj2_19](https://user-images.githubusercontent.com/20802925/116993096-e5963900-acce-11eb-8727-efec0efc1351.PNG)

## Step 4 — Configuring Nginx to Use PHP Processor

Moving on to the next stage of the installation, I created the root web directory and assigned ownership as follows;

![Proj2_20](https://user-images.githubusercontent.com/20802925/116993873-f1362f80-accf-11eb-83b9-d52acb645f80.PNG)

I opened the configuration file using the nano command and modified it with the configuration text provided.

![Proj2_22](https://user-images.githubusercontent.com/20802925/116994086-30fd1700-acd0-11eb-9778-ffbe09a09e82.PNG)

I activated the configuration by linking to the config file from Nginx’s sites-enabled directory and tested my configuration for syntax errors.

![Proj2_24](https://user-images.githubusercontent.com/20802925/116994443-a1a43380-acd0-11eb-8cd7-a80d73c98f30.PNG)

I disabled the default nginx host and reloaded nginx to apply the changes. I also created and index.html file in the web root folder to test the new server block.

![Proj2_25](https://user-images.githubusercontent.com/20802925/116994783-11b2b980-acd1-11eb-80fc-212587683e54.PNG)

I opened the website using the IP address.

![Proj2_26](https://user-images.githubusercontent.com/20802925/116995152-9bfb1d80-acd1-11eb-9a93-cfdcafe6d1af.PNG)

## Step 5 – Testing PHP with Nginx

I proceeded to test to validate nginx handling of .php files by creating a test PHP file and configuring it as directed.

![Proj2_27](https://user-images.githubusercontent.com/20802925/116996117-da450c80-acd2-11eb-9692-8a092236cadc.PNG)

![Proj2_28](https://user-images.githubusercontent.com/20802925/116996442-50497380-acd3-11eb-9249-adc3ac4c673d.PNG)

I then accessed the page via my browser by appending /info.php to the public IP address of the server.

![Proj2_29](https://user-images.githubusercontent.com/20802925/116996477-635c4380-acd3-11eb-880b-47f62c3d9bb7.PNG)

The info.php file was then removed.

![Proj2_30](https://user-images.githubusercontent.com/20802925/116997031-2a709e80-acd4-11eb-9b01-26c9a7176ee6.PNG)

## Step 6 — Retrieving data from MySQL database with PHP

To carry out step 6, I connected back into MySQL

![Proj2_31](https://user-images.githubusercontent.com/20802925/116997271-7de2ec80-acd4-11eb-87c7-e9dab3cdd319.PNG)

I created a database using a different database name from the one in the instruction.

![Proj2_30](https://user-images.githubusercontent.com/20802925/116997495-c4384b80-acd4-11eb-9165-ce8f59e7429e.PNG)

I created a user and modified the password from the one used in the instructions and granted database permission to the user. Then I exited MySQL.

![Proj2_36](https://user-images.githubusercontent.com/20802925/116998041-8c7dd380-acd5-11eb-80be-131030ca3516.PNG)

I tested the new user's permissions by logging back into MySQL using the user credentials created earlier.

![Proj2_37](https://user-images.githubusercontent.com/20802925/116998257-d797e680-acd5-11eb-92ab-dd8c89fca43d.PNG)

I confirmed that the user had access to the database.

![Proj2_38](https://user-images.githubusercontent.com/20802925/116998426-19289180-acd6-11eb-9a9b-684871832be4.PNG)

I attempted to create the test table but encountered some errors.

![Proj2_40](https://user-images.githubusercontent.com/20802925/116999038-019dd880-acd7-11eb-857e-099d296738a1.PNG)
















