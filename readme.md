# SpyMods

A lightweight and easy-to-deploy application packaged with Docker for fast installation and reliable performance.

## Features

* Dockerized for simple deployment
* Easy setup and configuration
* Production-ready container image
* Lightweight and optimized build
* Cross-platform support

## Prerequisites

Before running SpyMods, make sure you have:

* Docker installed
* Docker Compose (optional)

## Pull the Image

```bash
docker pull marcofinn/spymods:latest
```

## Run the Container

```bash
docker run -d \
  --name spymods \
  -p 3000:3000 \
  marcofinn/spymods:latest
```

## Docker Compose

```yaml
version: "3.8"

services:
  spymods:
    image: marcofinn/spymods:latest
    container_name: spymods
    restart: unless-stopped
    ports:
      - "3000:3000"
```

Start the application:

```bash
docker compose up -d
```

## Environment Variables

Configure your application using environment variables.

| Variable     | Description                | Required |
| ------------ | -------------------------- | -------- |
| APP_ENV      | Application environment    | Yes      |
| APP_PORT     | Application port           | No       |
| DATABASE_URL | Database connection string | Yes      |

## Updating

Pull the latest image and restart the container:

```bash
docker pull marcofinn/spymods:latest
docker restart spymods
```

## Support

If you encounter any issues, please open an issue in the GitHub repository.

## License

This project is licensed under the MIT License.
