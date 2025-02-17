# Docker Compose Project

This repository contains a Docker Compose setup for managing your multi-container Docker applications.

## Getting Started

### Prerequisites

- Docker: [Install Docker](https://docs.docker.com/get-docker/)
- Docker Compose: [Install Docker Compose](https://docs.docker.com/compose/install/)

### Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/your-repo.git
    cd your-repo
    ```

2. Start the Docker containers:
    ```sh
    docker-compose up -d
    ```

3. Verify that the containers are running:
    ```sh
    docker-compose ps
    ```

## Usage

### Accessing Services

- Service 1: [http://localhost:8080](http://localhost:8080)
- Service 2: [http://localhost:8081](http://localhost:8081)

### Stopping the Containers

To stop the running containers:
```sh
docker-compose down
```

## Modifying the Docker Compose Configuration

### Adding a New Service

1. Open the `docker-compose.yml` file.
2. Add a new service definition under the `services` section. For example:
    ```yaml
    services:
      new-service:
        image: new-service-image
        ports:
          - "8082:80"
    ```

3. Save the file and start the new service:
    ```sh
    docker-compose up -d
    ```

### Changing Service Configuration

1. Open the `docker-compose.yml` file.
2. Modify the configuration for the desired service. For example, to change the port mapping:
    ```yaml
    services:
      existing-service:
        ports:
          - "8083:80"
    ```

3. Save the file and restart the service:
    ```sh
    docker-compose up -d existing-service
    ```

## Troubleshooting

### Viewing Logs

To view the logs for a specific service:
```sh
docker-compose logs <service-name>
```

### Rebuilding Containers

If you need to rebuild the containers (e.g., after changing the Dockerfile):
```sh
docker-compose up --build -d
```

## Contributing

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes.
4. Commit your changes (`git commit -m 'Add new feature'`).
5. Push to the branch (`git push origin feature-branch`).
6. Open a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
