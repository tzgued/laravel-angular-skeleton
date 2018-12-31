# Docker-Laravel-Angular

This project is a docktorized skeleton for a laravel and angular Application.

## Requirements

    1. Docker
    2. Gitbash (For Windows users Only)
    3. Git (For linux and MAC OS users)

## Instalation Steps

### 1- Cloning the repo

    To clone the repo open your terminal in your projects directory and use this line:

    ```
    git clone https://github.com/tzgued/laravel-angular-skeleton.git ChooseAProjectName
    ```

    or this line if you are using ssh:
    
    ```
    git clone git@github.com:tzgued/laravel-angular-skeleton.git ChooseAProjectName
    ```
### 2- Setting up the environement variables

    - Copy the `docker/.env.example` file into `docker/.env`
    - Copy the `api/.env.example` file into `api/.env`
    - Change the variables in each file as it suits you (if you are new to this, and you have no server running on your machine, you can use the default environnement variables)

### 3- Create docker containers

    - `cd ' into the `docker ` folder
    - exacute `docker-compose up -d `
    - Sit back and relax for a while

    What this will do ? This will:
        - Pull docker images if you don't have them
        - Create the containers using the `docker-compose.yml ` file, and the `config ` and `Dockerfiles `
        - Install tools needed inside the containers

### 4 Installing dependencies

