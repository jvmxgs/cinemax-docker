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
### Docker commands

## 1. Start the services
Start the containers if they are stopped:
```bash
docker start cinemax-back
docker start cinemax-front
```

## 2. Stop the services
Stop the running containers:

```bash
docker stop cinemax-back
docker stop cinemax-front
```

## 3. Restart the services
Restart the containers:

```bash
docker restart cinemax-back
docker restart cinemax-front
```

## 4. Remove the services (containers)
Stop and remove the containers:

```bash
docker rm -f cinemax-back
docker rm -f cinemax-front
```

## 5. Build or rebuild images (Docker Compose)
If you are using docker-compose to manage your services, you can rebuild the images:

```bash
docker-compose build cinemax-back
docker-compose build cinemax-front
```

## 6. Rebuild and restart (Docker Compose)
Force the image rebuild and restart the containers:

```bash
docker-compose up --build cinemax-back
docker-compose up --build cinemax-front
```

##  7. Bring up services with docker-compose
Bring up or start the services defined in docker-compose.yml:

```bash
docker-compose up -d cinemax-back
docker-compose up -d cinemax-front
```

## 8. Stop services with docker-compose
Stop the services without removing the containers:

```bash
docker-compose stop cinemax-back
docker-compose stop cinemax-front
```

## 9. Remove services with docker-compose
Stop and remove the containers, networks, and volumes created by docker-compose:

```bash
docker-compose down
```

## 10. View logs
Get the logs from the services:

```bash
docker logs cinemax-back
docker logs cinemax-front
```

To continuously follow the logs in real-time:

```bash
docker logs -f cinemax-back
docker logs -f cinemax-front
```
