## IMPLEMENT A CLIENT SERVER ARCHITECTURE USING MYSQL DATABASE MANAGEMENT SYSTEM (DBMS)
Hello, welcome to my Project 5 implementation file. I will share my implementation of a client server architecture using MYSQL DBMS with screen shots and brief notes.

# Launch Two EC2 Instances To Serve As Client & Server
<img width="960" alt="p1" src="https://user-images.githubusercontent.com/20802925/134778017-9356ccb4-53bc-4694-85ff-37b8a2133762.PNG">

I connected to the server instance using ssh
<img width="957" alt="p2" src="https://user-images.githubusercontent.com/20802925/134778120-26aa7ab1-7a68-4c32-8ab7-b2d1e845bf4d.PNG">

<img width="936" alt="p3" src="https://user-images.githubusercontent.com/20802925/134778128-fc11c804-c48b-4ce6-9659-838ef23d8fdc.PNG">

I performed sudo apt update and sudo apt upgrade on the sql server instance

<img width="960" alt="p4" src="https://user-images.githubusercontent.com/20802925/134778258-95449c6a-3b68-40c0-9df6-5f534f3219ae.PNG">

<img width="960" alt="p5" src="https://user-images.githubusercontent.com/20802925/134778269-bd7cbf8b-55a6-4c47-a8ab-81980d7f2eeb.PNG">

<img width="958" alt="p6" src="https://user-images.githubusercontent.com/20802925/134778280-54a54d59-6e52-472a-8fc3-b49bd3229734.PNG">

<img width="960" alt="p7" src="https://user-images.githubusercontent.com/20802925/134778291-d782acc7-9b30-4b94-9a4a-5ed3dfbbfed4.PNG">

I installed mysql server software on the sql server instance

<img width="960" alt="p8" src="https://user-images.githubusercontent.com/20802925/134778334-74f9f178-6e6f-4eba-918a-903677a90444.PNG">

<img width="960" alt="p9" src="https://user-images.githubusercontent.com/20802925/134778341-565c83c6-4c23-49d5-a050-7d911d98ea7d.PNG">

I ran the command to secure the mysql server installation

<img width="960" alt="p10" src="https://user-images.githubusercontent.com/20802925/134778433-e57882e0-c116-4cf6-80c1-ac2591b17c78.PNG">

<img width="960" alt="p11" src="https://user-images.githubusercontent.com/20802925/134778444-64374a3c-e16a-422c-8676-24ab20b60bc5.PNG">

<img width="960" alt="p12" src="https://user-images.githubusercontent.com/20802925/134778449-5e8429d4-d8d8-49aa-96c9-1dc8baf5f674.PNG">

I created a database on the mysql server instance and a database user

<img width="960" alt="p15" src="https://user-images.githubusercontent.com/20802925/134778518-7e392651-ea9e-4ce6-a7a2-28dbe4ef7647.PNG">

I then opened another terminal and logged in to the client instance. I performed the sudo apt update and sudo apt upgrade commands

<img width="960" alt="p16" src="https://user-images.githubusercontent.com/20802925/134778596-b6a76a83-8416-4b9a-bc64-6893881a7c50.PNG">

<img width="960" alt="p17" src="https://user-images.githubusercontent.com/20802925/134778603-8d7406dd-1985-4dc2-a3b6-663badb52990.PNG">

<img width="956" alt="p18" src="https://user-images.githubusercontent.com/20802925/134778614-795d2c31-2592-4996-a0e5-4d0e49e4bb52.PNG">

<img width="960" alt="p19" src="https://user-images.githubusercontent.com/20802925/134778627-0a8c40cf-164d-4d2a-bf96-b369194f683e.PNG">

I installed the mysql client software on the client instance

<img width="960" alt="p20" src="https://user-images.githubusercontent.com/20802925/134778661-dded1539-13f7-41de-88d1-1e54607eca3d.PNG">

<img width="960" alt="p21" src="https://user-images.githubusercontent.com/20802925/134778670-a59187e9-9508-4749-be6d-aafd927605b3.PNG">

On the server instance I edited the bind address in the configuration file

<img width="960" alt="p22" src="https://user-images.githubusercontent.com/20802925/134778722-48b22837-f3e8-45b6-a8d1-924643c51abd.PNG">

<img width="960" alt="p23" src="https://user-images.githubusercontent.com/20802925/134778730-014dfdef-0c3b-443e-ab6f-7ff16c049492.PNG">

I edited the inbound rules on the server instance security group to accept a connection from the client server using the private IP address of the client server

<img width="952" alt="p24" src="https://user-images.githubusercontent.com/20802925/134778820-6c5636e1-c722-49c5-9dba-df5212c65ff9.PNG">

<img width="960" alt="p25" src="https://user-images.githubusercontent.com/20802925/134778836-50b645a9-06fa-4738-bdb9-94d9d5d278fe.PNG">

I went back to the mysql server terminal and granted database access to the user created earlier

<img width="960" alt="p26" src="https://user-images.githubusercontent.com/20802925/134778994-41f2b877-bdde-4047-b96c-897a95a31d42.PNG">

<img width="960" alt="p27" src="https://user-images.githubusercontent.com/20802925/134779003-f9b7fe57-9aef-4a86-a604-d435b6edc89c.PNG">

From the mysql client instance, I connected to the database in the mysql server instance and confirmed that I was connected to the database by running the SHOW DATABASES command to display the database name created earlier. Project complete. Thank you.

<img width="960" alt="p28" src="https://user-images.githubusercontent.com/20802925/134779491-6486942c-29f5-45da-b39c-2afc2fc6a2ac.PNG">

<img width="960" alt="p29" src="https://user-images.githubusercontent.com/20802925/134779501-661dab51-14dd-4160-892a-6b3f2720e9c4.PNG">

<img width="960" alt="p30" src="https://user-images.githubusercontent.com/20802925/134779507-94669f78-6d6e-492a-a2f8-1559bfb52e83.PNG">


