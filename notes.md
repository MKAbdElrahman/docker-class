
# docker images
In object-oriented programming (OOP), a class is like a blueprint for creating objects, and an object is an instance of a class. Similarly, a Docker image is like a blueprint for creating Docker containers, and a Docker container is an instance of a Docker image.

When you create a container from an image, you are essentially creating a new instance of that image that runs in its own isolated environment. The container has its own file system, networking, and resources, which are all separate from the host system and any other containers running on the same host.

Just like how you can create multiple instances of an object from the same class, you can create multiple instances of a container from the same image. Each container will be isolated from the others and will have its own set of running processes.



# `docker images ls`
The command "docker image ls" lists all the Docker images that are currently available on your Docker host. The output will include information such as the repository and tag name of each image, its unique image ID, the size of the image, and when it was created. Here is an example output:

```
REPOSITORY                     TAG       IMAGE ID       CREATED         SIZE
nginx                          latest    ae2feff98a0c   4 weeks ago     133MB
mysql                          latest    4a415e366388   2 months ago    544MB
ubuntu                         latest    4e2eef94cd6b   4 months ago    73.9MB
```

In this example, you can see that there are three images listed: nginx, mysql, and ubuntu. The "latest" tag refers to the most recent version of each image. The "IMAGE ID" is a unique identifier for each image, which can be used to reference it in other Docker commands. The "CREATED" column shows when each image was created, and the "SIZE" column shows the size of the image.
# docker container run -d --rm --name quantum --publish mode=ingress,published=18080,target=8080 docker.io/spkane/quantum-game:latest

The `docker container run` command you provided is used to start a new Docker container from the `spkane/quantum-game` image. Here is a breakdown of the various options used in the command:

- `-d`: This option runs the container in detached mode, which means that it runs in the background and the terminal is immediately available for other commands.

- `--rm`: This option tells Docker to automatically remove the container when it exits. This is useful for temporary containers that are only needed for a single task.

- `--name quantum`: This option assigns a name to the container. In this case, the name is set to `quantum`.

- `--publish mode=ingress,published=18080,target=8080`: This option publishes a container's port(s) to the host. In this case, it publishes port 8080 in the container to port 18080 on the host. The `mode=ingress` option specifies that the published port should be reachable from outside the Docker swarm cluster.

- `docker.io/spkane/quantum-game:latest`: This is the name of the image that the container is based on. The `latest` tag specifies that the most recent version of the image should be used.

So, overall, this command starts a new Docker container named `quantum` based on the `spkane/quantum-game` image, runs it in detached mode, publishes port 8080 in the container to port 18080 on the host, and automatically removes the container when it exits.


# `docker container ls`

The `docker container ls` command is used to list all running Docker containers on your Docker host. This command is an alias for the `docker ps` command with specific options.

# `docker container stop containerNameoOrID`