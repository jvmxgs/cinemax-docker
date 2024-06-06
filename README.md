# cinemax Docker

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

## Running the System

5. Start the system using Docker Compose, which will build the necessary containers:

    ```bash
    docker-compose up --build
    ```
