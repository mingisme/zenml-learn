# ZenML Docker Deploy

This project sets up a ZenML server with MySQL backend using Docker Compose.

## Setup Instructions

### 1. Create Project Directory

```bash
mkdir zenml-docker-deploy
cd zenml-docker-deploy
```

### 2. Initialize Poetry Project

```bash
poetry init
```

### 3. Add Dependencies

```bash
poetry add setuptools
poetry add zenml
```

### 4. Create Docker Compose Configuration

Create a `docker-compose.yml` file with the ZenML server and MySQL configuration.

### 5. Start the Services

```bash
docker compose -p zenml up -d
```

### 6. Access the ZenML Dashboard

```bash
poetry run zenml login http://localhost:8080
```

The ZenML dashboard will be available at http://localhost:8080

## Services

- **ZenML Server**: Runs on port 8080
- **MySQL Database**: Runs on port 3306 with root password `password`

## Stopping the Services

```bash
docker compose -p zenml down
```
