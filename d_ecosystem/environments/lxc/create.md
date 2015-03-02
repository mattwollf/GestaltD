#Create a Linux Container Image

[GestaltD](../README.md) → [LXC](./README.md) → [create](./create.md)

##Foreword

Creating an Linux container is straight-forward. 
Essentially, **lxc** clones an existing template which you should be aware of from the [last tutorial](./install.md). 
We will be using the **lxc-ubuntu** template for most of the work we do here.

##Prerequisites
###Required
* [Install](./install.md) lxc and lxc-templates

###Optional

##Core Instruction
> Create a container named **d_virt_env** from the **ubuntu** template.

    user@host ~ $ sudo lxc-create -t ubuntu -n d_virt_env

>> Notice there are two flags:
>>> **-n** This is the name of your container.

>>> **-t** This is the container template you want to use.

> You don't need to call your container **d_virt_env**, 
> you can name it whatever you want. 

> However, for the purposes of this tutorial we will call it **d_virt_env** 
> because this tutorial is about creating a virtual environment for D.

> **Note:** At the end of generation, the default username and password of the container 
> will be printed to the screen.
> Write this down, or at least take a mental note of it.
> You will need this later.

##Quick Test
###Check that our container image was successfully created.
> The easiest way to find our new container is to use **lxc-ls**

    user@host ~ $ sudo lxc-ls

> You should see the container you just created. 
> You will see others if you have created them as well. 

> If we do a further cursory check in **/var/lib/lxc**

    user@host ~ $ cd /var/lib/lxc/

> We get the following error:

    bash: cd: /var/lib/lxc/: Permission denied

> This directory is protected for security reasons.
> However we can still **ls** into the directory to see its contents if we have **sudo** permissions.

    user@host ~ $ sudo ls /var/lib/lxc/
    d_virt_env

> If you can see the container image you created, this step should be successful.

##Experimenting
> If we add an additional flag **-P </path/to/directory/>** 
> we can change the directory where our contaner is stored.

    user@host ~ $ sudo lxc-create -n d_virt_env -t ubuntu -P ~

> Here we are choosing to store it in our home directory (**/home/user/d_virt_env/**)

> **Note:** This may fail depending on permissions, 
> but that's OK, because we will be using the default directory anyway.

##RTFM
    user@host ~ $ man lxc-create

> As always the **man** pages are a wealth of information. 
> Notably, we find out the "**object directory**" (the image for our container) 
> is stored in **/var/lib/lxc/** by default.

    user@host ~ $ lxc-create --help

> Is also helpful for a quick understanding of our options.

##Critical Thinking
* Why is **/var/lib/lxc/** locked down so securely?

* What is the first thing you are going to remember to do when you log into this container? (Hint: It's a matter of security)

* What is the initial size of your new image?

##Review
> Having completed this tuorial you should now be able to:

* Create a container image for your virtual environment.

* Read the **man** pages for **lxc-create**.

* Find flags for **lxc-create**.

* Change the install directory for your image.

* Find the default **username** and **password** for your container image.

##Next steps.
* [Start](./start.md) your virtual environment.

##Learn More
