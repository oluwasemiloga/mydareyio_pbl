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

![Proj3_33](https://user-images.githubusercontent.com/20802925/117877394-67bcc980-b29c-11eb-9149-d96da6924cf4.PNG)












