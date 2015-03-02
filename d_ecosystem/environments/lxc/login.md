#Log into an LXC container
[GestaltD](../README.md) → [LXC](./README.md) → [login](./login.md)

##Foreword

Finally, we can use our Linux container. If you've used **ssh** before, 
this should be second nature to you. Otherwise, it's pretty easy.

##Prerequisites
###Required
* Get your Linux container's vital [info](./info.md)

###Optional
* Install **ssh** on your host machine.

##Core Instruction

> Log into the **d_virt_env** container as if it were an individual machine.

> You should have written the default **username** and **password** from the 
> previous "[Create](./create.md) a Linux Container Image" tutorial.
> If you didn't it is username: **ubuntu**, password: **ubuntu**

> You should have also written the IP address from the previous 
> "Get [Information](./info.md) About Your Linux Container Image" tutorial. 
> If you don't have that you are going to have to go back to that tutorial 
> and retrieve it.

###Log in via ssh
> The recommended method of connecting is via **ssh**

    user@host ~ $ ssh ubuntu@<IP Address>

> You will be prompted to confirm the container's identity.
> Type:

    yes

> When prompted.

> Then you will be prompted for a password. Remember, it is **ubuntu**.

###Alternative: Log in without ssh
> However, if you played around during the "[Start](./start.md) a Linux Container Image" 
> tutorial you would know that you can also log in simply by starting the 
> container without the **-d** (daemon) flag.

    user@host ~ $ sudo lxc-start -n d_virt_env

> Enter the username and password when prompted.

###Congratulations, you are now using your Linux container
> You will notice your prompt has changed from:

    user@host ~ $ 

> To:

    ubuntu@d_virt_env:~$ 

> It's important to note that this tutorial will follow these conventions. 
> So, take note as sometimes you will need to work on your host and sometimes 
> you will need to work inside your container.

###Change your default password
> This may not be too important, but it is good practice to change your default 
> password. If only because it is the first password everyone will try if they 
> want to comprimise the system.

> However, you might want to keep the default password if you are planning on 
> sharing your container with others later.

    ubuntu@d_virt_env:~$ passwd

###Exit from the container
> Pretty self explanitory:

    ubuntu@d_virt_env:~$ exit

> You should be back in your host shell.

##RTFM
> First, check out passwd

    ubuntu@d_virt_env:~$ man passwd

> **WTF???** **man** pages don't work inside the container?
> Containers are "light-weight" and only come with the bare minimum. **man** pages 
> don't make the cut. However, you can install them easily:

    ubuntu@d_virt_env:~$ sudo apt-get install man

> OK, **NOW** check out the docs on passwd:

    ubuntu@d_virt_env:~$ man passwd

> Likewise, you'll probably want to brush up on **ssh** if you don't have a strong grasp on it.

    ubuntu@d_virt_env:~$ man ssh

##Quick Test
> If you got this far, it's probably working.

##Experimenting
> Play around inside your Linux container as if it were a workstation and 
> get a feel for similarities and differences. It's a disposable environment, 
> so try and break it. 
> If you manage to FUBAR it that's OK, you can make another one!

##Critical Thinking
* Can you disable the default user altogether and substitute a custom user?

##Review
> Having completed this tuorial you should now be able to:

* Log in to your container via **lxc-start** and **ssh**

* Install **man** pages (if you need to)

* Change the container's default password.

* Exit from the container.

##Next Steps
* [Install DMD](/dmd/README.md)

##Learn More
