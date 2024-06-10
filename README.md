# Cinemax Docker

This repository contains the Docker setup for the cinemax project, including the frontend and backend components. Follow the steps below to set up and run the system locally.

## Prerequisites

Before you begin, ensure you have the following installed:

- [Git](https://git-scm.com/)
- [Docker](https://www.docker.com/get-started)

## Installation

1. Clone the repository and navigate to the project directory:

    ```bash
    git clone git@github.com:jvmxgs/cinemax-docker.git
    cd cinemax-docker/
    ```

2. Initialize and update the submodules:

    ```bash
    git submodule update --init --recursive
    ```

3. Make sure that both repos are in main branch, if not change to main branches:

    ```bash
    cd cinemax-back
    git switch main
    
    cd ../cinemax-front
    git switch main
    ```
4. Return to main folder:

    ```bash
    cd ../
    ```

## Running the System

5. Start the system using Docker Compose, which will build the necessary containers:

    ```bash
    docker-compose up --build
    ```

## Project Running Status

The project should be running smoothly now.

### Access URLs:
- Frontend: [http://localhost:5173/](http://localhost:5173/)
- Backend: [http://localhost:9000/](http://localhost:9000/)

### Credentials:
- **Email**: `test@example.com`
- **Password**: `password`


## API Documentation:
[https://documenter.getpostman.com/view/36131674/2sA3XLG52Z](https://documenter.getpostman.com/view/36131674/2sA3XLG52Z)


## Troubleshooting Docker Project Build Issues

If you encounter any problems with the Docker project build, you can access the services as follows:

### Database Migrations Issue:
- Access the backend service:
  ```bash
  docker exec -it cinemax-back sh
  ```
- Run the following command to refresh and seed the database:
  ```bash
  php artisan migrate:fresh --seed
  ```

### NPM Packages Issue:
- Access the frontend service:
  ```bash
  docker exec -it cinemax-front sh
  ```
- Run the following command to install npm packages:
  ```bash
  npm install
  ```
