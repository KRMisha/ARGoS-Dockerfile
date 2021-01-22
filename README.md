# ARGoS Dockerfile

A Dockerfile to containerize the [ARGoS](https://github.com/ilpincy/argos3) simulator and its [examples](https://github.com/ilpincy/argos3-examples).

## Prerequisites

- [Docker](https://docs.docker.com/engine/install/)
- [x11docker](https://github.com/mviereck/x11docker)

## Setup

1. Clone the repo and cd into it:

    ```sh
    git clone https://github.com/KRMisha/ARGoS-Dockerfile.git
    cd ARGoS-Dockerfile
    ```

2. Build the image:

    ```sh
    docker build . -t argos
    ```

## Usage

1. Start the container interactively with x11docker:

    ```sh
    x11docker -i --hostdisplay argos
    ```

2. Run one of the ARGoS experiment examples:

    ```sh
    cd /argos3-examples
    argos3 -c experiments/diffusion_10.argos
    ```

    A simulator window should now appear.

3. To exit the container, press `Ctrl+D` or use the `exit` command.
