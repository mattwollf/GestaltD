#Installing LXC on your Ubuntu host

##Foreword

Installation of Linux containers is pretty straight forward. 
Everything required is availible in Ubuntu's apt repository.

##Prerequisites

* [Install Ubuntu](/ubuntu/README.md).

* Your user must have **sudo** privileges.

## Instruction

> The First thing you want to do is install **lxc** from the apt repository

    user@host ~ $ sudo apt-get install lxc lxc-templates

> This will install **lxc** along with some generic templates. 

> Included in the **lxc-templates** package is the "ubuntu" template, which is what we will use for each tutorial.

##RTFM
    user@host ~ $ man lxc

> The **man** pages for **lxc** is a good place to start if you are new to Linux containers.

> If you have a question the first rule is always RTFM. Go ahead and do it now.

##Quick Test
###Check if LXC has been installed

> If the you were successful in reading the **man** pages, you are probably set.
> Let's do some further exploration.

> Another helpful technique is to see what is installed is to type:

    user@host ~ $ lxc<TAB><TAB>

> (Press the **<Tab>** key a couple of times to auto complete a command in Linux).

> This will bring up a list of programs starting with "lxc-"

    user@host ~ $ lxc-
    lxc-attach           lxc-destroy          lxc-start
    lxc-autostart        lxc-device           lxc-start-ephemeral
    lxc-cgroup           lxc-execute          lxc-stop
    lxc-checkconfig      lxc-freeze           lxc-unfreeze
    lxc-clone            lxc-info             lxc-unshare
    lxc-config           lxc-ls               lxc-usernsexec
    lxc-console          lxc-monitor          lxc-wait
    lxc-create           lxc-snapshot 

> We will go over some of these in later tutorials. You don't need to worry too much about them now.
> But it is well enough to know what is installed.

> The above listed programs **should** be installed in **/usr/bin/**
> You can check that they exist in that location now.

    user@host ~ $ cd /usr/bin/

    user@host ~ $ ls lxc*

> You should see the same list as before.

> If these steps are successful, congratulations. LXC should be installed.

###Check if the templates have been installed.

> Now let's test if our templates have been installed.
> Change directory to **/usr/share/lxc/templates/**

    user@host ~ $ cd /usr/share/lxc/templates/

> List the contents of the present working directory (pwd)

    user@host ~ $ ls

> You should see a list of files (a dozen or so).
> The one we will most be interested in is: **"lxc-ubuntu"**.
> But it is good to have an idea of where templates are stored and which ones are availible.

> If you can verify **lxc** has been installed and verify **lxc-templates** have been installed, you can continue.

##Experimenting
> There are other packages in the repository related to lxc besides the ones we installed.
> You can see what they are by entering the following:

    user@host ~ $ sudo apt-get install lxc<tab><tab>

> They are out of the scope of this tutorial, but install them and understand them if it interests you.

##Critical Thinking
* Can you provide a short discription of what a Linux Container is? (Hint: RTFM)

* Why is using LXC advantagious to using a virtual machine?

* Why is using LXC advantagious to using chroot?

##Review
> Having completed this tuorial you should now be able to:

* Install LXC
* Install LXC templates
* Read the **man** pages for **lxc**
* Find the installation directory for **lxc**
* Find the installation directory for **lxc-templates**

## Next steps.
* [Create](./create.md) a new virtual environment

## Learn More
