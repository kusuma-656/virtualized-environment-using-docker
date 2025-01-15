# Docker Setup Instructions

Follow the steps below to set up and run a Redis container using Docker.

## Prerequisites
- Ensure VS Code Editor has installed on the local system.
- Download and install Docker Desktop from the official website.

---

## Steps

### Step 1: Create a New Folder
1. Open the terminal or file explorer.
2. Create a new folder for the project.
3. Open the folder in VS Code.

---

### Step 2: Write a Dockerfile
1. Inside the folder, create a new file named `Dockerfile` (no file extension).
2. Add the following content to the file:
    ```dockerfile
    FROM alpine
    RUN apk add --update redis
    CMD ["redis-server"]
    ```

---

### Step 3: Build and Run the Docker Image
1. Open the terminal in VS Code or any preferred terminal.
2. Execute the following commands:
    ```bash
    docker build -t kusuma/redis:latest .  --> to build the image
    docker run kusuma/redis                --> Running the container
    ```

---

### Step 4: Verify the Container and Image
1. List the running containers:
    ```bash
    docker ps 
    ```

2. List Docker images:
    ```bash
    docker images
    ```

3. Stop the running container using its container ID:
    ```bash
    docker stop <container_id>
    ```

---

## Notes
- Replace `<container_id>` with the actual container ID from the `docker ps` command.
- Ensure Docker Desktop is running before executing Docker commands.

---
