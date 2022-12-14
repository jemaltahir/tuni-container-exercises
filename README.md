# Tuni-container-exercises

## Exercise A

### 1 The purpose of this exercise is to introduce you to Redhat container tools, specifically Podman. We will install Podman, verify the Podman client is installed in our OS, and test it by running an image from a remote registry using Podman available (API  alls) commands.  

1.1 Introducing Redhat container available tools.

Take a look at the output of the following command in your terminal. There you will find the version of the container tools and how often they are updated, as well as the current version (latest version).

```sh
sudo yum module list | grep container-tools
```

1.2 Install latest Podman conatiner.

In the official documentation for [Podman](https://podman.io/getting-started/installation), it is explained how to install it for various OSes.

```sh
sudo yum -y install podman
```

1.3 Verify installation.

```sh
podman --help
podman version
```

1.4 Running first container.

Get familiarized yourself with logs in the terminal after running the following command.

`podman run hello`

1.5 Extra (Modify Podman container search list registries).

Add "registry.fedoraproject.org" to the "unqualified-search-registries" search list erntries.
N.B Careful when adding registries only add registries that are trusted registries such as official images.

(Hint!!!) `/etc/containers/registries.conf`

### 2 In this exercise, we will explore Podmans basic commands such as pull, run, stop, and remove.

2.1 Pulling Podman image
In this exercise, we will get familiar with the Podman basic commands. Let's pull some images from registries as follows:

```sh
podman pull nginx
podman pull ubuntu
```

This Podman pull command will cache images locally from remote registries. Let's take a look at the following command to list cached images locally.

```sh
podman images 
```

2.2 Now let's start to run the container as a background process and later we will inspect it while it is running in the background. To start a container as a background process we will issue the following command: 

```sh
podman run -itd --name myos ubuntu bash
```

List all containers running in the system (use podmans help)?

We can refer to the container using CONAINER ID or container name in our case myos.

Enter into the one of the running container in your OS, for example conatiner myos, and run a shell command `ls` then finally `exit` command? Consult podman help.

2.3 Now lets stop the running conatiner.

Stop the running container myos? and confirm using a command that the myos is stopped? Observe that the state of the conatiner! What is the current state of the container? What does it mean?

consult podman help.

2.4 Finally let's remove  

Before removing the container you can restart it or delete it permanently.

Restart, stop and delete the conatiner ?  And verify that the conatiner deleted permannently?

consult podman help.

### 3 Container port forwarding and digging information 

In this exercise we will work on container publishing ports to be accessible from the host OS and inspect the running container to get more information about the container.

3.1 Running an application container and publish a port to host OS.

```sh
podman run -d -p 8080:80 nginx
```

Now the nginx application is up and running and ready to serve for incoming request.

Check the availability of the service using `curl` command ?

Why do you think is this command `podman run -d -p 80:80 nginx` is not working ?

Explore how to make it work ?

Inspect the nginx container???s "NetworkSettings",  "Cmd", "CreateCommand", and  PortBindings.

### 4 

### 5 Build and tag custom container image. 



