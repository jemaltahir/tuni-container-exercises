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
Now let's start to run the container as a background process and later we will inspect it while it is running in the background. To start a container as a background process we will issue the following command: 
