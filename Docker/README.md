
![Docker-Temporary-Image-Social-Thumbnail-1200x630-1](https://github.com/mutasim77/knowledge-sharing/assets/96326525/29775a8f-3d2f-4240-9260-bcb8a1e6395a)

# Docker 🐳 
Welcome to my Docker repository! Here, I'll explain Docker in simple terms with easy-to-understand examples. 

Docker 🐳 can seem like a complex concept at first glance. Many people have a basic understanding of what Docker is, but they often struggle to grasp its full potential and practical applications. 

That's where this repository comes in. 🔗

# Table of Contents 📜

Explore Docker step-by-step:

- [Introduction to Docker 🚀](#introduction-to-docker-)
- [Getting Started 🏁](#getting-started-)
  - [Installation and Setup ⚙️](#installation-and-setup-)
  - [Running Your First Container 🏃‍♂️](#running-your-first-container-)
- [Dockerfile Basics 📄](#dockerfile-basics-)
  - [Writing a Dockerfile ✍️](#writing-a-dockerfile-)
- [Understanding Images 🖼️](#understanding-images-)
  - [What are Docker Images? 📸](#what-are-docker-images-)
  - [Creating Your Own Images 🎨](#creating-your-own-images-)
  - [Pulling and Pushing Images 🚚](#pulling-and-pushing-images-)
- [Working with Containers 🛠️](#working-with-containers-)
  - [Managing Containers 📦](#managing-containers-)
  - [Interacting with Containers 💬](#interacting-with-containers-)
- [Docker Compose 🚢](#docker-compose-)
  - [What is Docker Compose? 🎵](#what-is-docker-compose-)
  - [Writing Docker Compose Files 📝](#writing-docker-compose-files-)
  - [Docker Compose Commands 🛠](#docker-compose-commands-)
- [Advanced Topics 🔍](#advanced-topics-)
  - [Networking 🌐](#networking-)
  - [Volumes 📂](#volumes-)
  - [Security 🔒](#security-)



# Introduction to Docker 🚀
Alright, let's take a trip down memory lane! Remember those days when you were a kid, playing with your favorite toys and building awesome stuff with LEGO bricks? Well, Docker is a bit like those days, but for your computer!

Imagine you're back in your room, surrounded by all your toys. But instead of toys, think of these as different computer programs or apps you use every day. Now, just like you had your special toy box to keep things organized, Docker gives each of these apps its own little box to stay in.

But here's where it gets really cool: these boxes, called containers, aren't just ordinary boxes. They're like magical containers that can hold all the stuff an app needs to work perfectly, just like how your toy box had all the pieces your LEGO castle needed.

So, Docker basically helps your computer keep everything tidy and running smoothly, just like how you kept your toys neat and organized back in the day. Cool, right?

Now, let's dive a bit deeper into what Docker is all about and how it can make your life easier!


# Getting Started 🏁
Let's roll up our sleeves and get started with Docker! Just like learning to ride a bike or bake cookies, getting started with Docker is all about taking those first few steps.

## Installation and Setup ⚙
First things first, we need to get Docker up and running on your computer. It's like getting your bike ready for a ride or preheating the oven before baking cookies. Don't worry, though, it's easier than you think!

1. **Choose Your Platform:** Visit [Docker's website](https://docs.docker.com/get-docker/) and choose your operating system (Windows, macOS, or Linux).
2. **Read System Requirements:** Before downloading, make sure to read the system requirements carefully to ensure compatibility with your computer.
3. **Download Docker:** After confirming compatibility, proceed with the download by clicking on the appropriate button. This will start the download process.
4. **Install Docker:** Once the download is complete, run the installer by double-clicking on the downloaded file. Follow the on-screen instructions to complete the installation process. It's just like installing any other program.
5. **Start Docker:** After installation, start up Docker on your computer. You'll usually find it in your applications or system tray.
 
And that's it! Docker is now installed and ready to go on your computer.

## Running Your First Container 🏃‍♂
Now that Docker is set up, let's dive in and run your very first container. It's like taking your bike for a spin around the block or putting your cookie dough in the oven for the first time. Exciting, right?

1. **Open Docker:** Start up Docker on your computer if you haven't already.
2. **Open Terminal or Command Prompt:** We'll need to use a terminal or command prompt to interact with Docker.
3. **Run a Container:** Use the `docker run` command followed by the name of an image to run a container. For example, you can run a simple "Hello, World!" container like this:
```bash
docker run hello-world
```
4. **See the Magic Happen:** Docker will download the necessary image and run it in a container. You'll see a message confirming that Docker is up and running.

And there you have it! You've just run your first Docker container. Pretty cool, huh?

# Dockerfile Basics 📄
Now that you've got Docker up and running, let's explore Dockerfiles! Think of Dockerfiles as recipes for creating your own custom containers. It's like following a recipe to bake your favorite cookies!

## Writing a Dockerfile ✍
Writing a Dockerfile is easy and fun! It's all about telling Docker how to build your container step by step. Let's break it down:
1. **Create a New File:** Start by creating a new text file in your favorite code editor. You can name it anything you like, but conventionally it's called `Dockerfile`.
2. **Define the Base Image:** Every Dockerfile starts with a `FROM` instruction, where you specify the base _image_ for your container. This is like choosing the type of dough for your cookies.
For example:
```bash
FROM ubuntu:latest
```
3. **Add Instructions:** Now it's time to add more instructions to your Dockerfile. These instructions tell Docker what to install and how to configure your container. It's like adding ingredients and mixing them together in your cookie recipe.

For example:
```bash
# Use the official Python image from Docker Hub
FROM python:3.9

# Set the working directory inside the container
WORKDIR /app

# Copy the requirements file into the container
COPY requirements.txt requirements.txt

# Install the dependencies specified in requirements.txt
RUN pip install -r requirements.txt

# Copy the rest of the application files into the container
COPY . .

# Specify the command to run the application
CMD ["python", "app.py"]
```
In this Dockerfile:
- We start by specifying a base image using `FROM python:3.9`, which is an official Python image from Docker Hub.
- We set the working directory inside the container to `/app` using `WORKDIR`.
- We copy the `requirements.txt` file from our local directory into the container using `COPY`.
- We install the Python dependencies listed in `requirements.txt` using `pip install -r requirements.txt`.
- We copy the rest of the application files (assuming they are in the same directory as the Dockerfile) into the container using `COPY`.
- Finally, we specify the command to run the application when the container starts using `CMD ["python", "app.py"]`.

> _<sub>This Dockerfile is ready to build a Docker image for a Python application.</sub>_

4. **Build Your Image:** Once you've written your Dockerfile, it's time to build your custom image. Open a terminal or command prompt, navigate to the directory containing your Dockerfile, and run the docker build command.
```bash
docker build -t my-custom-image .
```
> _<sub>This will build your image according to the instructions in your `Dockerfile` and tag it with the name `my-custom-image`. </sub>_

5. **Run Your Container:** Finally, you can run your container using the image you just built. It's like baking your cookies and enjoying the delicious results!

> And there you have it! You've written your first Dockerfile and built your own custom container. Now you're ready to create all sorts of amazing containers for your applications! 🪄

# Understanding Images 🖼
Docker revolves around images. But what exactly are Docker images, and how do they work?

## What are Docker Images? 📸
Docker images are like snapshots of your applications. Imagine them as frozen moments captured in a photo frame. Each image contains everything your application needs to run smoothly: the code, libraries, settings, and more. It's like having a complete recipe for your favorite dish, with all the ingredients listed and ready to go.

## Creating Your Own Images 🎨
Creating your own Docker images is like crafting your own masterpiece. You start with a base image, which is like the foundation of your artwork. Then, you add layers of customization, just like adding layers of paint to a canvas. Each layer builds upon the previous one until you have a unique creation that perfectly suits your needs. It's similar to following a recipe but adding your own special twist to make it truly yours.

Remember when we wrote a Dockerfile? That's exactly how we create our own Docker images. We specify the base image, add any additional dependencies or configurations, and Docker builds it all into a neat package, just like following a recipe to bake your favorite cake.

## Pulling and Pushing Images 🚚
Docker makes it easy to share and distribute images, just like sharing recipes with friends. You can pull images from Docker Hub, which is like a giant recipe book filled with images created by others. When you want to try out a new dish, you pull the recipe from the book (or in this case, pull the image from Docker Hub) to your kitchen (or local machine).

And when you've perfected your own recipe and want to share it with the world, you can push your images to Docker Hub for others to enjoy. It's like publishing your cookbook for everyone to see and try out your delicious creations.

> [!IMPORTANT]
> Here's the link to the Docker Hub: [link](https://hub.docker.com/)

# Working with Containers 🛠
Containers are the heart of Docker. Let's explore how to work with them effectively.

## Managing Containers 📦
Managing containers is like orchestrating a kitchen. You have multiple dishes cooking simultaneously, and you need to keep track of each one to ensure they're all running smoothly.

- _**Starting a Container**_: To start a container, you use the `docker run` command followed by the name of the image. It's like putting a dish into the oven to start cooking.
```bash
docker run my-image
```

 - _**Stopping a Container**_: To stop a container, you use the `docker stop` command followed by the container's ID or name. It's like taking a dish out of the oven when it's done cooking.
```bash
docker stop my-contain
```

 - _**Viewing Running Containers**_: To see a list of running containers, you use the `docker ps` command. It's like peeking into the kitchen to see what's currently cooking.
```bash
docker ps
```

## Interacting with Containers 💬
Interacting with containers is like tasting your dishes to ensure they're seasoned just right.

 - _**Executing Commands**_: You can execute commands inside a running container using the `docker exec` command. It's like giving instructions to your chef while they're cooking.
```bash
docker exec -it my-container bash
```

 - _**Viewing Container Logs**_: To view the logs generated by a container, you use the `docker logs` command followed by the container's ID or name. It's like reading the recipe to see if everything is going according to plan.
```bash
docker logs my-container
```

> [!IMPORTANT]
> - Just like managing a busy kitchen, working with containers in Docker requires careful orchestration and attention to detail. By starting, stopping, and interacting with containers, you're essentially overseeing a kitchen full of dishes, ensuring everything runs smoothly and deliciously.
> - With Docker's simple yet powerful commands, you can effortlessly manage and monitor your containers, just like a chef oversees their culinary creations. By mastering container management, you gain greater control over your software development process, enabling you to serve up perfectly cooked applications every time.
> - Now that you've got the basics down, let's dive deeper into the world of Docker and explore more advanced techniques to elevate your container cooking skills!

# Docker Compose 🚢
Docker Compose is like having your own sous chef in the kitchen, helping you manage complex recipes with ease.

## What is Docker Compose? 🎵
Docker Compose is a tool for defining and running multi-container Docker applications. It's like having a recipe book for your entire meal, with each dish carefully planned out and prepared to perfection.

With Docker Compose, you can specify all the services and configurations for your application in a single YAML file, making it easy to manage and deploy your entire stack. It's like having all your ingredients laid out on the counter, ready to be combined into a delicious feast.

## Writing Docker Compose Files 📝
Writing Docker Compose files is like creating a master plan for your culinary masterpiece. Let's create a Docker Compose example for setting up a PostgreSQL server along with a PgAdmin container for managing it:
```yml
version: '3.8'

services:
  db:
    image: postgres:latest
    environment:
      POSTGRES_DB: mydatabase
      POSTGRES_USER: myuser
      POSTGRES_PASSWORD: mypassword
    ports:
      - "5432:5432"
    volumes:
      - pgdata:/var/lib/postgresql/data

  pgadmin:
    image: dpage/pgadmin4:latest
    environment:
      PGADMIN_DEFAULT_EMAIL: admin@example.com
      PGADMIN_DEFAULT_PASSWORD: admin
    ports:
      - "8080:80"
    depends_on:
      - db

volumes:
  pgdata:
```

In this Docker Compose file:

- We define two services: `db` for the PostgreSQL database and `pgadmin` for PgAdmin.
- For the **db** service:
  - We use the official *postgres:latest* image.
  - We set environment variables for the database name, user, and password.
  - We expose port *5432* on the host and map it to port 5432 in the container for PostgreSQL connections.
  - We use a volume named *pgdata* to persist the PostgreSQL data.
- For the pgadmin service:
  - We use the *dpage/pgadmin4:latest* image for PgAdmin.
  - We set environment variables for the default login credentials.
  - We expose port *8080* on the host and map it to port 80 in the container for PgAdmin access.
  - We specify that the *pgadmin* service depends on the *db* service, ensuring that PgAdmin starts after PostgreSQL is up and running.\


## Docker Compose Commands 🛠
Managing Docker Compose projects is a breeze with a set of handy commands. Let's explore some essential ones:

### Starting and Stopping Services 🚀
To start your Docker Compose project, simply navigate to the directory containing your `docker-compose.yml` file and run:
```bash
docker-compose up
```
This command will build (if necessary) and start all the services defined in your Compose file.

To stop your project and shut down all services, use:
```bash
docker-compose down
```

### Viewing Service Logs 📜
To view the logs for all services in your Docker Compose project, use:
```bash
docker-compose logs
```
This command will display logs from all services, helping you troubleshoot any issues or monitor the behavior of your containers.

### Executing Commands in Services 📡
You can execute commands within a specific service container using `docker-compose exec`. For example, to open a shell in the `web` service:
```bash
docker-compose exec web sh
```
This command allows you to interact directly with containers, making it easy to debug or perform administrative tasks.

### Viewing Service Status 📊
To view the status of services defined in your Docker Compose project, use:
```bash
docker-compose ps
```
This command provides a quick overview of which services are running, stopped, or paused, similar to checking the status of dishes in a busy kitchen.

### Starting and Stopping Services 🚀
To start or stop specific services in your Docker Compose project, you can use:
```bash
docker-compose start
```
and 
```bash
docker-compose stop
```
These commands allow you to control the lifecycle of your services, just like turning on or off burners on a stove.

### Pausing and Killing Services ⏸️💥
To pause or kill specific services in your Docker Compose project, you can use:
```bash
docker-compose pause
```
and
```bash
docker-compose kill
```
Pausing a service temporarily stops its execution without removing it, similar to putting a dish on hold. Killing a service forcefully terminates it, like removing a dish from the menu entirely.

> [!IMPORTANT]
> - Docker Compose is a powerful tool for orchestrating multi-container Docker applications, simplifying the development and deployment process. With a concise YAML file and a handful of commands, you can define, manage, and scale your entire application stack effortlessly.
> - While we've covered Docker Compose basics, it's important to note that there are many more commands and options available to suit your specific needs. By mastering Docker Compose, you gain greater control and flexibility over your containerized applications, allowing you to focus on building and delivering exceptional software solutions.
