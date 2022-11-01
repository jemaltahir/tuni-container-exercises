# Tuni-container-exercises

## Exercise A

The purpose of this exercise is to introduce you to Redhat container tools, specifically Podman. We will install Podman, verify the Podman client is installed in our OS, and test it by running an image from a remote registry using Podman available (API  alls) commands.  

1.0 Introducing Redhat container available tools.

Take a look at the output of the following command in your terminal. There you will find the version of the container tools and how often they are updated, as well as the current version (latest version).

```sh
sudo yum module list | grep container-tools
```

1.1 Install latest Podman conatiner.

In the official documentation for [Podman](https://podman.io/getting-started/installation), it is explained how to install it for various OSes.

```sh
sudo yum -y install podman
```

1.2 Verify installation.

```sh
podman --help
podman version
```

1.3 Running first container.

Get familiarized yourself with logs in the terminal after running the following command.

`podman run hello`

1.4 Extra (Modify Podman container search list registries).

Add "registry.fedoraproject.org" to the "unqualified-search-registries" search list erntries.
N.B Careful when adding registries only add registries that are trusted registries such as official images.



