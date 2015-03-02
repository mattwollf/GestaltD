#Using LXC (Linux Containers) as a D virtual environment.
[GestaltD](../README.md) → [LXC](./README.md)

##Foreword
Linux containers (LXC) are a fairly simple way to manage your D ecosystem without 
having to worry about it messing up your current workstation.

For the uninitiated, an LXC might be thought of as something between chmod and 
a virtual machine.
Like chmod, a process is restricted to specific privileges in a machine.
However, from the aspect of the processes inside it; LXC resembles a full-blown 
Linux OS.
The advantages are that, (compared to a virtual machine), one does not need to 
fully allocate a block of memory / hard drive space / processor cores. These are 
all dynamically allocated as they are needed by the container.

In addition, here are some other reasons for using LXC in your workflow:

* Your virtual environment is kept separate from your working environment.
* Untrusted code / libraries on your virtual environment can not affect your workstation environment.
* Your workstation environment will not affect your virtual environment.
* You can have several separate virtual environments which do not conflict with each other.
* Virtual environments are easier to standardize.
* Virtual environments can be shared amongst workgroups.

While using LXC isn't required, This tutorial series will assume you are using 
LXC containers.

##Conventions
You may come across the following conventions while reading this tutorial series:
    username@host ~ $
    ubuntu@d_virt_env ~ $
This will probably look familiar, obviously it is a command prompt.
    username
should be understood to be a substiture for your workstation's username. 
    ubuntu
should be understood to be the default username for a Linux container created from 
the ubuntu lxc-template. You can change this, and probably should for security reasons. However for 
the purposes of this tutorial series, we keep the default.
    @host
if host is identified, it should be understood that you are executing this 
command on your workstation, not your virtual environment.
    @d_virt_env
if d_virt_env is identified, it should be understood that you are executing this 
command in your virtual environment. If you are not using a virtual environment 
you can substitute this for the name of the workstation you are executing from. 
Additionally, you may choose to call your virtual environment something other 
than "d_virt_env", for instance, you can name it after your project. This is 
fine. However, understand we will consistantly call it d_virt_env in this 
tutorial series.

##Prerequisites
###Required
* [Install Ubuntu](/ubuntu/README.md)

##Table of Contents
* [GestaltD](/README.md)
    * [LXC](./README.md)
    * [Install](./install.md) LXC
    * [Create](./create.md) a new D virtual environment (LXC container)
    * [Start](./start.md) d_virt_env
    * Get d_virt_env [info](./info.md)
    * d_virt_env [Login](./login.md)
    * [Destroy](./destroy.md) d_virt_env
    * [Share](./share.md) d_virt_env with your workgroup

##Next steps.
[Installation Guide](./install.md)

##Learn More
[linuxcontainers.org](https://linuxcontainers.org/)

