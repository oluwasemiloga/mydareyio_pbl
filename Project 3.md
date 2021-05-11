# Simple To-Do application on MERN Web Stack

Hello, welcome to my Project3 implementation file. I will share my implementation of a simple To-Do application on MERN web stack with screen shots and brief notes.

I set up my EC2 Instance of t2.micro family with Ubuntu Server 20.04 LTS (HVM) image.

![Proj3_1](https://user-images.githubusercontent.com/20802925/117697979-0bce4400-b1bb-11eb-9fb0-14541212c156.PNG)

![Proj3_2](https://user-images.githubusercontent.com/20802925/117697991-0f61cb00-b1bb-11eb-8d25-787c5c480216.PNG)

I downloaded & launched MobaxTerm and opened up a session to ssh into my Ubuntu EC2 instance. Very quick & easy to use.

![Proj3_3](https://user-images.githubusercontent.com/20802925/117698622-d24a0880-b1bb-11eb-9994-06417bddeaa6.PNG)

![Proj3_4](https://user-images.githubusercontent.com/20802925/117698628-d413cc00-b1bb-11eb-991b-17692b117b0d.PNG)

![Proj3_5](https://user-images.githubusercontent.com/20802925/117698643-d6762600-b1bb-11eb-83ab-e40505ca7d84.PNG)

## Step 1 - Backend configuration

I updated and upgraded my Ubuntu instance with the given commands.

![Proj3_6](https://user-images.githubusercontent.com/20802925/117699174-6d42e280-b1bc-11eb-8513-e1e91c477435.PNG)

![Proj3_7](https://user-images.githubusercontent.com/20802925/117699179-6fa53c80-b1bc-11eb-8461-e11b10dd1967.PNG)

![Proj3_8](https://user-images.githubusercontent.com/20802925/117699193-72079680-b1bc-11eb-8cfc-75bae9fca765.PNG)

![Proj3_9](https://user-images.githubusercontent.com/20802925/117699199-73d15a00-b1bc-11eb-8885-1319c4d6b77d.PNG)

# Install Node.js on the server

I installed Node.js using the appropriate commands

![Proj3_10](https://user-images.githubusercontent.com/20802925/117699634-fb1ecd80-b1bc-11eb-8ff7-d8fc3c88a5aa.PNG)

![Proj3_11](https://user-images.githubusercontent.com/20802925/117699640-fc4ffa80-b1bc-11eb-9214-11225bdc64e7.PNG)

![Proj3_12](https://user-images.githubusercontent.com/20802925/117699663-0245db80-b1bd-11eb-8267-67d4ffd56350.PNG)

Node.js & npm installation verified.

![Proj3_13](https://user-images.githubusercontent.com/20802925/117700096-7da78d00-b1bd-11eb-97a4-281b6f69d660.PNG)

# Application Code Setup

I created a new directory called Todo, verified the directory with the ls command and then changed into the new directory with the cd command.

![Proj3_15](https://user-images.githubusercontent.com/20802925/117702062-f0196c80-b1bf-11eb-87c2-b9fa1b83c27d.PNG)

I ran the npm init command to initialize the project and create the package.json file.

![Proj3_16](https://user-images.githubusercontent.com/20802925/117870593-36d89680-b294-11eb-91ef-e7676c1b4c53.PNG)

# Install ExpressJS

Install express

![Proj3_17](https://user-images.githubusercontent.com/20802925/117870873-9afb5a80-b294-11eb-82fe-a2f9269282f4.PNG)

I created the index.js file.

![Proj3_18](https://user-images.githubusercontent.com/20802925/117870989-c3835480-b294-11eb-8170-ad3038e629cc.PNG)

I installed the dotenv module.

![Proj3_19](https://user-images.githubusercontent.com/20802925/117872447-946de280-b296-11eb-96b9-d3543478fb6d.PNG)

I opened the index.js file using vim and pasted in the code provided.

![Proj3_20](https://user-images.githubusercontent.com/20802925/117874288-ad779300-b298-11eb-97f8-81df19f8762c.PNG)

I ran the node index.js command but didn't get the output specifying port 5000. I played around with the code a few times which still didn't work. Eventually I went into the index.js file again and deleted and recopied the code and it worked as expected. I edited my security group inbound rules to open TCP port 5000. Browser access using the public IP address was also successful.

![Proj3_24](https://user-images.githubusercontent.com/20802925/117875099-b026b800-b299-11eb-8195-02b1386b86e0.PNG)

![Proj3_25](https://user-images.githubusercontent.com/20802925/117875498-25928880-b29a-11eb-8fe0-27f0aac14337.PNG)

# Routes

I created the routes directory.

![Proj3_26](https://user-images.githubusercontent.com/20802925/117875966-b23d4680-b29a-11eb-8c00-8154ce10087a.PNG)

I changed into the routes directory and created the api.js file.

![Proj3_27](https://user-images.githubusercontent.com/20802925/117876142-eca6e380-b29a-11eb-9b9c-2d4319e8cab4.PNG)

I opened the api.js file and copied in the code.

![Proj3_28](https://user-images.githubusercontent.com/20802925/117876380-3bed1400-b29b-11eb-980d-c64e3dcd7c42.PNG)

![Proj3_29](https://user-images.githubusercontent.com/20802925/117876391-3e4f6e00-b29b-11eb-97b4-15e6c47b1e74.PNG)

# Models

I changed back to the Todo folder and installed Mongoose.

![Proj3_30](https://user-images.githubusercontent.com/20802925/117876679-90908f00-b29b-11eb-928d-a88b05e5b816.PNG)

The new models directory and todo.js file were created.

![Proj3_31](https://user-images.githubusercontent.com/20802925/117877103-0bf24080-b29c-11eb-9515-66005880dc2f.PNG)

I opened the todo.js file and pasted in the provided code.

![Proj3_32](https://user-images.githubusercontent.com/20802925/117877386-64c1d900-b29c-11eb-8f86-a778f1c66cf9.PNG)

![Proj3_99](https://user-images.githubusercontent.com/20802925/117879879-5d4fff00-b29f-11eb-91a6-6759669bca74.PNG)

I updated the api.js file with the code provided to make use of the new model.

![Proj3_33](https://user-images.githubusercontent.com/20802925/117880342-e7986300-b29f-11eb-8c0e-ebc0829a99f3.PNG)

# MongoDB Database

I created the MongoDB database following the instructions and retrieved the connection string.

![Proj3_36](https://user-images.githubusercontent.com/20802925/117881648-65a93980-b2a1-11eb-953b-92cda4cba158.PNG)

I created the .env file and opened it to add the database connection string.

![Proj3_40](https://user-images.githubusercontent.com/20802925/117882032-d4869280-b2a1-11eb-801b-77ec8c9da819.PNG)

![Proj3_41](https://user-images.githubusercontent.com/20802925/117882121-ea945300-b2a1-11eb-9844-4ea7aabb2291.PNG)

I then updated the index.js file with the code provided

![Proj3_42](https://user-images.githubusercontent.com/20802925/117883452-56c38680-b2a3-11eb-8c08-7cd359689eaa.PNG)

![Proj3_43](https://user-images.githubusercontent.com/20802925/117883464-588d4a00-b2a3-11eb-8207-62ff0ebd6654.PNG)

I proceeded to start my server using the node index. js command. I was unable to connect to my database and got an error message.

![Proj3_44](https://user-images.githubusercontent.com/20802925/117884232-465fdb80-b2a4-11eb-8cc8-6e0af8b88a1c.PNG)

I decided to see if I could find a way to resolve the error so I performed a google search using the text from the error message.

![Proj3_50](https://user-images.githubusercontent.com/20802925/117884676-d56cf380-b2a4-11eb-8b91-4e1726972532.PNG)

![Proj3_51](https://user-images.githubusercontent.com/20802925/117884684-d7cf4d80-b2a4-11eb-9f59-a7aa6912d61f.PNG)

One of the solutions suggested a password update of the database using the autogenerate password function so I tried that.

![Proj3_46](https://user-images.githubusercontent.com/20802925/117885027-372d5d80-b2a5-11eb-9e8f-d22b749df7ac.PNG)

![Proj3_47](https://user-images.githubusercontent.com/20802925/117885033-38f72100-b2a5-11eb-8618-e1f09641156d.PNG)

![Proj3_48](https://user-images.githubusercontent.com/20802925/117885036-3b597b00-b2a5-11eb-8098-90c7aaad1f58.PNG)

I then updated my connection string in the .env file. I ran the node index.js command again and was able to connect successfully to the database :)

![Proj3_49](https://user-images.githubusercontent.com/20802925/117885412-bf136780-b2a5-11eb-8abd-3435db698c21.PNG)

![Proj3_45](https://user-images.githubusercontent.com/20802925/117885416-c175c180-b2a5-11eb-9571-79d385270362.PNG)

# Testing Backend Code without Frontend using RESTful API

I downloaded and installed postman.

![Proj3_52](https://user-images.githubusercontent.com/20802925/117886163-b4a59d80-b2a6-11eb-9ecd-fa38d87225f2.PNG)

I created a post request to the API.

![Proj3_53](https://user-images.githubusercontent.com/20802925/117886378-051cfb00-b2a7-11eb-8377-2469d8c436ac.PNG)

![Proj3_54](https://user-images.githubusercontent.com/20802925/117886387-077f5500-b2a7-11eb-8401-964e5c7bed66.PNG)

I then created a get request and received a response.

![Proj3_56](https://user-images.githubusercontent.com/20802925/117886989-ebc87e80-b2a7-11eb-80cc-9cedfaa93b3d.PNG)

![Proj3_57](https://user-images.githubusercontent.com/20802925/117886992-ee2ad880-b2a7-11eb-97a1-5d18fc2c3969.PNG)

I attempted the optional task of sending a DELETE request using the ID and was able to do so successfully. I ran the GET request again and saw that the entry had been removed.

![Proj3_58](https://user-images.githubusercontent.com/20802925/117887597-e28be180-b2a8-11eb-9170-90c517022ba5.PNG)

![Proj3_59](https://user-images.githubusercontent.com/20802925/117887601-e455a500-b2a8-11eb-9416-848c9d030862.PNG)

![Proj3_60](https://user-images.githubusercontent.com/20802925/117887605-e6b7ff00-b2a8-11eb-8a74-c472763fd6d8.PNG)

# Step 2 - Frontend creation

I ran the create-react-app command. The client folder was also created.

![Proj3_61](https://user-images.githubusercontent.com/20802925/117888006-73fb5380-b2a9-11eb-9b69-d4e37b5359c1.PNG)

![Proj3_63](https://user-images.githubusercontent.com/20802925/117888304-c63c7480-b2a9-11eb-8070-02429a869451.PNG)

# Running a React App

Concurrently and nodemon were installed.

![Proj3_64](https://user-images.githubusercontent.com/20802925/117888536-216e6700-b2aa-11eb-9cf0-a7bfa2ce2db1.PNG)

![Proj3_65](https://user-images.githubusercontent.com/20802925/117888540-23d0c100-b2aa-11eb-8307-3933392db217.PNG)

![Proj3_66](https://user-images.githubusercontent.com/20802925/117888548-26331b00-b2aa-11eb-9384-397b5aa26b42.PNG)

![Proj3_67](https://user-images.githubusercontent.com/20802925/117888554-28957500-b2aa-11eb-8bc5-f88a91c2193f.PNG)

In my Todo folder I opened the package.json file and modified the code as directed.

![Proj3_68](https://user-images.githubusercontent.com/20802925/117888816-8629c180-b2aa-11eb-8c82-49ea29df0273.PNG)

![Proj3_69](https://user-images.githubusercontent.com/20802925/117888824-87f38500-b2aa-11eb-9761-44cf62883ba6.PNG)


# Configure Proxy in package.json

I changed to the client directory and opened the package.json file and added the key value pair as directed to enable browser access. I opened a TCP port 3000 on my security group inbound rules.

![Proj3_70](https://user-images.githubusercontent.com/20802925/117889595-bf166600-b2ab-11eb-843a-9ae0d324f754.PNG)

![Proj3_71](https://user-images.githubusercontent.com/20802925/117889601-c2115680-b2ab-11eb-8455-95bb24b0146c.PNG)

![Proj3_72](https://user-images.githubusercontent.com/20802925/117889802-0997e280-b2ac-11eb-927f-d08f8941995f.PNG)

I ran the npm run dev command but it failed to execute and I received some error messages. I watched the project 3 implementation video and discoverd that I had placed the key value pair in the package.json file in the wrong position. When I adjusted this my npm run dev command executed successfully.

![Proj3_73](https://user-images.githubusercontent.com/20802925/117890719-9d1de300-b2ad-11eb-99e1-e7f1faeec73c.PNG)

![Proj3_74](https://user-images.githubusercontent.com/20802925/117891012-14ec0d80-b2ae-11eb-8692-388c217d35dc.PNG)

![Proj3_93](https://user-images.githubusercontent.com/20802925/117891019-19b0c180-b2ae-11eb-8cb1-267105fa3a56.PNG)

![Proj3_95](https://user-images.githubusercontent.com/20802925/117891028-1d444880-b2ae-11eb-9bec-7e8993336597.PNG)

![Proj3_81](https://user-images.githubusercontent.com/20802925/117891170-58df1280-b2ae-11eb-939b-c7defbbe86a4.PNG)

# Creating your React Components

From the src directory in the client directory, I created the components folder. I then created three files Input.js, ListTodo.js and Todo.js.

![Proj3_76](https://user-images.githubusercontent.com/20802925/117891646-2e418980-b2af-11eb-8ed8-e15015f48241.PNG)

In the input.js the provided code was pasted.

![Proj3_77](https://user-images.githubusercontent.com/20802925/117891822-8082aa80-b2af-11eb-804c-f9eb8b9f75d3.PNG)

Axios was installed from the client folder.

![Proj3_79](https://user-images.githubusercontent.com/20802925/117892145-174f6700-b2b0-11eb-8185-4d8f5a544b74.PNG)

![Proj3_82](https://user-images.githubusercontent.com/20802925/117892234-3b12ad00-b2b0-11eb-8d9c-c2784949b62c.PNG)

From the components directory I opened the ListTodo.js file and pasted the code as directed.

![Proj3_83](https://user-images.githubusercontent.com/20802925/117892374-86c55680-b2b0-11eb-9940-ccc3b231599a.PNG)

![Proj3_84](https://user-images.githubusercontent.com/20802925/117892377-8927b080-b2b0-11eb-8c2e-8da363eb9cdb.PNG)

The Todo.js file was also modified with the code provided.

![Proj3_85](https://user-images.githubusercontent.com/20802925/117892573-e28fdf80-b2b0-11eb-84c2-da47734fc35f.PNG)

![Proj3_86](https://user-images.githubusercontent.com/20802925/117892579-e4f23980-b2b0-11eb-8b74-87a98f93ecd7.PNG)

From the src folder, the App.js file was modified as directed.

![Proj3_87](https://user-images.githubusercontent.com/20802925/117892724-2551b780-b2b1-11eb-9997-b49611028944.PNG)

![Proj3_88](https://user-images.githubusercontent.com/20802925/117892737-2b479880-b2b1-11eb-8420-ba7fcbdd26ef.PNG)

The App.css and index.css files are also modified as directed.

![Proj3_89](https://user-images.githubusercontent.com/20802925/117892937-73ff5180-b2b1-11eb-901c-f4093d222726.PNG)

![Proj3_90](https://user-images.githubusercontent.com/20802925/117892941-75c91500-b2b1-11eb-8da4-4503e3a82a2b.PNG)

![Proj3_91](https://user-images.githubusercontent.com/20802925/117892953-7792d880-b2b1-11eb-8641-43cd5035d71f.PNG)

![Proj3_92](https://user-images.githubusercontent.com/20802925/117892956-795c9c00-b2b1-11eb-9ba2-c050b7b1130a.PNG)

Going back to the Todo directory, the npm run dev command is executed. Update ToDo list.

![Proj3_100](https://user-images.githubusercontent.com/20802925/117895674-c98a2d00-b2b6-11eb-9753-737598cac16d.PNG)

Project completed. Thank you.
































