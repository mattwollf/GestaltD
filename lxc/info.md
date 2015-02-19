#Get Information About Your Linux Container Image

[GestaltD](../README.md) → [LXC](./README.md) → [info](./info.md)

##Foreword

We touched on **lxc-info** briefly in the [last](./start.md) segment. 
But this is a good time to get into detail about the rest of the information 
we get from this helpful command.

##Prerequisites
###Required
* [Start](./start.md) a Linux container image.

###Optional

##Core Instruction
> Get **d_virt_env**'s info

    user@host ~ $ sudo lxc-info -n d_virt_env
    Name:           d_virt_env
    State:          RUNNING
    PID:            13346
    IP:             10.0.3.186
    CPU use:        2.16 seconds
    BlkIO use:      316.00 KiB
    Memory use:     4.22 MiB
    Link:           veth69LUOW
     TX bytes:      24.76 KiB
     RX bytes:      15.70 KiB
     Total bytes:   40.46 KiB

> Relevant info is:

> **Name** You should already know this, but hey, just in case.

> **PID** You will probably need this later.

> **IP** you can use this to **ssh** into the container at any time. 
> Write this down.

> **CPU use**, **BlkIO use**, and **Memory use** are helpful for measuring the 
> vital stats of your Linux container.

> **Link** (and underlying stats **TX**, **RX**). Will be helpful when doing networking.

##RTFM
    user@host ~ $ man lxc-info

    user@host ~ $ lxc-info --help

> You get the idea. RTFM. It's important.

##Quick Test
> There isn't much to test here. 
> Just be aware of the information and how to get it.

##Experimenting
> RTFM and play with some of the flags. 

##Critical Thinking

##Review
> Having completed this tuorial you should now be able to:

* Get information about a running Linux container.

* RTFM.

* Identify vital stats.

* RTFM.

##Next steps.
* [Login](./login.md) to your virtual environment.

##Learn More
