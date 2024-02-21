# Docker Getting Started 

This repository is a sample application to start with a Docker container.


The .NET guide for beginners walks you through the process of creating a containerized .NET application using Docker. Throughout this tutorial, you'll gain proficiency in:

- Containerizing and running a .NET application
- Establishing a local development environment for .NET applications using containers

By completing the .NET getting started modules, you'll be equipped to containerize your own .NET application, drawing upon the examples and instructions provided in this comprehensive guide.



## Get the sample applications

In this guide, you will use a pre-built .NET application.
Open a terminal, change the directory to a directory that you want to work in, and
run the following command to clone the repository.

```console
 git clone https://github.com/didourebai/workshop2.git
```
## Initialize Docker assets

Now that you have an application, you can use `docker init` to create the
necessary Docker assets to containerize your application. Inside the
`docker-dotnet-sample` directory, run the `docker init` command in a terminal.
`docker init` provides some default configuration, but you'll need to answer a
few questions about your application. Refer to the following example to answer
the prompts from `docker init` and use the same answers for your prompts.

```console
$ docker init
Welcome to the Docker Init CLI!

This utility will walk you through creating the following files with sensible defaults for your project:
  - .dockerignore
  - Dockerfile
  - compose.yaml
  - README.Docker.md

Let's get started!

? What application platform does your project use? ASP.NET Core
? What's the name of your solution's main project? myWebApp
? What version of .NET do you want to use? 6.0
? What local port do you want to use to access your server? 8080
```

You should now have the following contents in your `docker-dotnet-sample`
directory.

```text
├── docker-dotnet-sample/
│ ├── .git/
│ ├── src/
│ ├── .dockerignore
│ ├── compose.yaml
│ ├── Dockerfile
│ ├── README.Docker.md
│ └── README.md
```
## Run the application

Inside the `docker-dotnet-sample` directory, run the following command in a
terminal.

```console
$ docker compose up --build
```

Open a browser and view the application at [http://localhost:8080](http://localhost:8080). You should see a simple web application.

In the terminal, press `ctrl`+`c` to stop the application.

### Run the application in the background

You can run the application detached from the terminal by adding the `-d`
option. Inside the `docker-dotnet-sample` directory, run the following command
in a terminal.

```console
$ docker compose up --build -d
```

Open a browser and view the application at [http://localhost:8080](http://localhost:8080). You should see a simple web application.

In the terminal, run the following command to stop the application.

```console
$ docker compose down
```
