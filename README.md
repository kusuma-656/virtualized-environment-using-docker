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
    docker build -t kusuma/redis:latest .  
    docker run kusuma/redis
    ```
    Above commands will build the image and run the container of the built image.

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
### Step 5: Basic Commands to Run in the Docker Environment
Below are essential Docker commands and their functionalities:

1. **Pull an image from Docker Hub:**
    ```bash
    docker pull <image_name>
    ```
    This command fetches the specified image from the Docker Hub repository.

2. **Run a Docker container from an image:**
    ```bash
    docker run <image_name>
    ```
    Starts a new container from the specified image.

3. **List running containers:**
    ```bash
    docker ps
    ```
    Displays details of all active containers.

4. **List all containers (active and stopped):**
    ```bash
    docker ps -a
    ```
    Shows details of all containers, including those that are stopped.

5. **List all Docker images:**
    ```bash
    docker images
    ```
    Lists all images stored on the system.

6. **Remove a stopped container:**
    ```bash
    docker rm <container_id>
    ```
    Deletes a container using its ID.

7. **Remove an image by name:**
    ```bash
    docker rmi <image_name>
    ```
    Removes the specified image from your system.

8. **Stop a running container:**
    ```bash
    docker stop <container_id>
    ```
    Stops a running container using its ID.


---

## Notes
- Replace `<container_id>` with the actual container ID from the `docker ps` command.
- Ensure Docker Desktop is running before executing Docker commands.

---
