#Start a Linux Container Image

[GestaltD](../README.md) → [LXC](./README.md) → [start](./start.md)

##Foreword

Starting a Linux container image is akin to booting a virtual machine.
The biggest difference is that the image's kernal and resources are shared 
with the host machine.

##Prerequisites
###Required
* [Create](./create) a Linux container image.

###Optional

##Core Instruction

> Start your D virtual environment (**d_virt_env**)

    user@host ~ $ sudo lxc-start -n d_virt_env -d

> Notice the flags:

> > **-n** We already know. This specifies the name of the image you want to start.

> > **-d** This is new. This flag specifies that we want to run this image as a daemon.


##RTFM
    user@host ~ $ man lxc-start

    user@host ~ $ lxc-start --help

> Go ahead and read these now. It only takes a second.

##Quick Test
###Check to see if your Linux container is running.
> If successful, you shouldn't have recieved any acknowledgement that your container 
> is running. This is good because, had it failed, you would have at least gotten a warning.

> We are jumping ahead here, but you can use **lxc-info** to get information about running containers.

    user@host ~ $ sudo lxc-info -n d_virt_env

> We will explore **lxc-info** in more detail in the next segment. 
> For now just note:

    State:         RUNNING

> If State is RUNNING, this tutorial has been successful.

##Experimenting
> Stop a Linux container using **lxc-stop**:

    user@host ~ $ sudo lxc-stop -n d_virt_env

> Now find its state using **lxc-info**, like before.

##Critical Thinking
* What happens if you don't run **lxc-start** as a daemon?

* Can you figure out what **lxc-monitor** does? (RTFM)

##Review
> Having completed this tuorial you should now be able to:

* Start a Linux Container as a daemon.

* RTFM.

* Get information about a running Linux container.

* Stop a running Linux container.

##Next steps.
* Get more [information](./info.md) about your virtual environment

##Learn More
