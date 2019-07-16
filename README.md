# Provide IBM Z (or LinuxONE) encryption capabilities to your s390x docker containers.
Container is the new service unit, much more than the Virtual Machine. Containers running on s390x processor architecture can count on the unique encryption features available on the IBM Z and LinuxONE platforms.

In this Code Pattern, you will pull and deploy a s390x docker container in a LinuxONE guest running in the LinuxONE Community Cloud.

The LinuxONE Community Cloud provides an open access to Linux running on a mainframe, primarily targeted at development, porting and functional testing. Registered users can deploy recent SLES and RHEL instances. It is an integrated environment that enables you to design, develop, deploy and manage on-premises, containerized cloud applications behind a firewall.

When you will complete this Code Pattern, you will understand how to:
* Configure a docker base image to adhere with the LinuxONE hardware cryptographic acceleration.
* Deploy this docker image, and use the new crypto facilities at the docker container level.
* Design a LinuxONE encryption dashboard with node-red.


# Architecture
This journey starts with a LinuxONE Linux guest which after some optimization will be able to claim hardware cryptographic assistance. From there, you will install docker, and deploy a docker container you will optimize in order to adhere with the s390x processor architecture.

# Included components

* [LinuxONE Crypto](https://www.ibm.com/it-infrastructure/linuxone/capabilities/secure-cloud)
* [OpenSSL](https://www.openssl.org/)
* [Curl](https://curl.haxx.se/)

# Featured technologies

* [Docker](https://www.docker.com/)
* [IBM LinuxONE](https://www.ibm.com/it-infrastructure/linuxone)

# Steps

## Step 1 - [Enabling Linux to use hardware encryption]

    1. Introduction to the pervasive encryption
    2. Introduction to the Linux crypto stack
    2. Enabling Linux to use the Hardware
    3. Enabling OpenSSL to use the hardware acceleration support
    4. Checking Hardware Crypto functions

## Step 2 - [Deploying a docker s390x base image running on LinuxONE Community Cloud.]
    
    1. What is docker?
    2. Installing docker
    3. Pulling a Docker base s390x image
    docker pull hyperledgerlinuxone/caasp

    docker run -it -p 1880:1880 --name mycaasp hyperledgerlinuxone/caasp:v2

    4. Deploying the Docker base image
    5. Optimizing the Docker base image
    6. Ultimately, knowing how to provide docker containers an access to a crypto card

## Step 3 - [Creating a simple crypto activity dashboard.]

    1. Accessing node-red
    2. Importing a node-red flow
    3. Using the node-red simple dashboard
    6. Testing your nodered dashboard
