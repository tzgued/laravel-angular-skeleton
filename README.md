# Docker-Laravel-Angular

This project is a docktorized skeleton for a laravel and angular Application.

## Requirements

1. Docker
2. Gitbash (For Windows users Only)
3. Git (For linux and MAC OS users)

## Installation Steps

### 1 - Cloning the repo

To clone the repo open your terminal in your projects directory and use this line:
```
git clone https://github.com/tzgued/laravel-angular-skeleton.git ChooseAProjectName
```

or this line if you are using ssh:
```
git clone git@github.com:tzgued/laravel-angular-skeleton.git ChooseAProjectName
```

Your projected is now cloned in the ChooseAProjectName directory

### 2 - Setting up the environement variables

- Copy the `docker/.env.example` file into `docker/.env` => `cp docker/.env.example docker/.env`
- Copy the `api/.env.example` file into `api/.env` => `cp api/.env.example api/.env`
- Change the variables in each file as it suits you (if you are new to this, and you have no server running on your machine, you can use the default environnement variables)

### 3 - Create docker containers

- `cd ` into the `docker ` folder    
- execute `docker-compose up -d `
- Sit back and relax for a while

What this will do ? This will:
- Pull docker images if you don't have them
- Create the containers using the `docker-compose.yml ` file, and the `config ` and `Dockerfiles `
- Install tools needed inside the containers

### 4 - SSH into container
> This and the rest of the steps could be automated but I didn't for the perpose of learning and knowing what's happening :)

Now we have our main container tha has all what needed to run the app: apache, php, node, angular CLI, ...
We need to ssh into the container and install composer and npm dependencies.
To ssh into a docker container use:

`docker exec -it Container_Name bash`

Gitbash users on widows might need to add `winpty` for the command to work

`winpty docker exec -it Container_Name bash`

### 5 - Installing the dependencies

Inside the container, our working directory is `/var/www/html/`
So now we need to `cd ` into `api ` and use `composer install ` and `npm install `
And we `cd ` into `front ` and use `npm install `

### 6 - Finally

Now you can `ng serve ` in the `front ` folder and have you Front and API apps available
To access your apps got to [http://localhost:8080](http://localhost:8080) 
Of course change the port to mach what you used in the .env file
