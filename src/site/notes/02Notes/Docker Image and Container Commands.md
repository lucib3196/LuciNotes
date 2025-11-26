---
{"dg-publish":true,"permalink":"/02-notes/docker-image-and-container-commands/","tags":["notes/atomic","cli/docker"]}
---

**Creation Date**: 2025-10-13 10:58

---

**General Things to know**: In docker when we see a single (`.`) that means we are referencing the current path. 

**Note**: These are just common commands, for a full list view [Docker Official CLI Commands](https://docs.docker.com/reference/cli/docker/)


## Reference Directory Structure

```bash
project/
├── src/ # The location of all the code 
│ ├── app.py
│── requirements.txt
│── Dockerfile
│── Dockerfile.dev # A docker file used for development
```

## Building 

These commands are focused on building a docker image

| Purpose                                                                                               | Command                                            | Example                                         | Notes                                                                                      |
| ----------------------------------------------------------------------------------------------------- | -------------------------------------------------- | ----------------------------------------------- | ------------------------------------------------------------------------------------------ |
| Build an image                                                                                        | `docker build -t <docker-name> .`                  | `docker build -t my_cool_app .`                 | Builds image from [[02Notes/Dockerfile\|Dockerfile]]  in current directory.  `-t` tags your image with a name. |
| How to build a docker image from a different docker file. Useful for cases such as a `Dockerfile.dev` | `docker build -f <target-file> -t <docker-name> .` | `docker build -f Dockerfile.dev -t myapp:dev .` |  The flag `-f` tells docker which file we want to use                                      |

## Running Containers

| Run a container                  | `docker run <image>`                       | docker run myapp              | Creates & runs a new container from the image                                                  |
| -------------------------------- | ------------------------------------------ | ----------------------------- | ---------------------------------------------------------------------------------------------- |
| Start a container using an ID    | `docker start <id>`                        | docker start 1234             |                                                                                                |
| Run with [[Port Mapping\|Port Mapping]]        | `docker run -p <host>:<container> <image>` | `docker run -p 8080:80 myapp` | Maps port 8080 on your machine to port 80 in container. For more info see: [[02Notes/Port Forwarding\|Port Forwarding]] |

## Removing Containers and images

| Stops a container based on an ID | `docker stop <container-id>` | docker stop 123abc | Gracefully stops container          |
| -------------------------------- | ---------------------------- | ------------------ | ----------------------------------- |
| Remove a container               | `docker rm <container_id>`   | `docker rm 123abc` | Deletes container, not image        |
| Remove an image                  | `docker rmi <image_id>`      | `docker rmi myapp` | Removes local image                 |
## Inspection and debugging

| Purpose                         | Command            | Example | Notes                               |
| ------------------------------- | ------------------ | ------- | ----------------------------------- |
| List all the running containers | `docker ps`        |         | Add `-a` to show stopped containers |
| Check Docker version            | `docker --version` |         | Verifies installation               |
| View Docker system info         | `docker info`      |         | Good for debugging issues           |

## Flags


| Flag   | Meaning                                                | Purpose                               | Example                                         |
| ------ | ------------------------------------------------------ | ------------------------------------- | ----------------------------------------------- |
| `-i`   | interactive (keep STDIN open)                          | To pipe code into the container       | `docker run -i python:3.11 python < script.py`  |
| `--rm` | remove after container stops                           | Cleanup; prevents leftover containers | `docker run --rm ubuntu echo "hello"`           |
| `-f`   | Specifies which file we want to use to build our image | Build from other Dockerfiles          | `docker build -f Dockerfile.dev -t myapp:dev .` |


## Workflow

A simple workflow for building an image and running

```python
from flask import Flask

app = Flask(__name__)

@app.route("/")
def home():
    return "Hello from Docker!"

if __name__ == "__main__":
    app.run(host="0.0.0.0", port=80)

```

```dockerfile
# Use a lightweight base image
FROM python:3.13-slim

# Set working directory
WORKDIR /app

# Copy everything into container
COPY . .

# Install dependencies
RUN pip install flask

# Expose port 80
EXPOSE 80

# Run the app
CMD ["python", "app.py"]

```

```bash 
docker build -t flask-hello .
docker run -p 8080:80 flask-hello
```

Open your browser at **[http://localhost:8080](http://localhost:8080)**


## Example with Docker Desktop

**Running `docker ps**
![Pasted image 20251011133742.png](/img/user/Attachments/Pasted%20image%2020251011133742.png)
![Pasted image 20251011133804.png](/img/user/Attachments/Pasted%20image%2020251011133804.png)

**Running `docker start**
![Pasted image 20251011134231.png](/img/user/Attachments/Pasted%20image%2020251011134231.png)



---
# More In Depth
- [[02Notes/Containerize a Python Application\|python container]] 