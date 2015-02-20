#Installing the D compiler DMD

[GestaltD](../README.md) → [DMD](./README.md) → [install](./install.md)

##Foreword

There are a number of compilers for the D language. 
However, I am going to focus specifically on **dmd**. 
This tutorial assumes you are logged into a [Linux container](/lxc/README.md) 
for a virtual environment. 
However, this is not strictly necessary you can probably follow along and 
install directly on your host.

##Prerequisites
###Required
* [Ubuntu](/ubuntu/README.md)

###Optional
* A running [LXC container](/lxc/README.md)

##Core Instruction
> Before you install, you are going to need to install some common tools.
> First of which is **wget**, which is a simplistic http client.
> All **wget** does is downloads a file.
> In this case, we will use it to download the compiler binaries.

    ubuntu@d_virt_env:~$ sudo apt-get install wget

> Now we are going to want a convenient place to download our files.
> You might have noticed that there are no directories in our home folder 
> by default in our Linux container. 
> If you are used to using an Ubuntu workstation, you might be familiar with 
> the **~/Downloads/** directory.
> So, we will create that now.

    ubuntu@d_virt_env:~$ mkdir ~/Downloads

> Now **cd** into that directory.

    ubuntu@d_virt_env:~$ cd ~/Downloads

> At the time I am writing this, dmd_2.066.1-0_amd64.deb is the latest stable 
> build. Double check http://downloads.dlang.org/releases/ for a newer release 
> or if you are using an architecture other than amd64 and replace it in the 
> command below.

    ubuntu@d_virt_env:~$ wget http://downloads.dlang.org/releases/2014/dmd_2.066.1-0_amd64.deb

> Now check to see if it downloaded to your **pwd**.

    ubuntu@d_virt_env:~$ ls
    dmd_2.066.1-0_amd64.deb

> If the file is in your directory, you are good to go.

> Now unpackage it. 
> dpkg is similar to apt-get except it installs packages already on your system.

    ubuntu@d_virt_env:~$ sudo dpkg --install ./dmd_2.066.1-0_amd64.deb

> You will probably get some dependency errors. That's OK. We can fix that 
> using the **-f** flag.

    ubuntu@d_virt_env:~$ sudo apt-get -f install

> After all the dependencies have been installed, **dmd** should also be installed.

##RTFM
> We will cover **dmd** in more detail in the following segments. 
> However, there isn't any reason why we can't RTFM before then.

    ubuntu@d_virt_env:~$ man dmd
    ubuntu@d_virt_env:~$ dmd --help

> **wget** is the real hero of this story though, so if you are unfamiliar, 
> take a moment to get aquainted. It's a useful tool.

    ubuntu@d_virt_env:~$ man wget
    ubuntu@d_virt_env:~$ wget --help

##Quick Test
###Check DMD is installed.
> You can check to see if **dmd** is installed by issuing the following command:

    ubuntu@d_virt_env:~$ dmd

> You should see output identical to **dmd --help**

##Experimenting
> We won't do much with dmd just yet. However, it should be noted, that, 
> like most packages, **dmd** is installed in **/usr/bin/** .
> Go ahead and check it out.

> While you are snooping around, check out **dmd**'s brother. **rdmd**.
> I won't spoil the suprise, but **rdmd** does some pretty cool things too.

##Critical Thinking
* Most distributions have **wget** installed by default. So, why did we have to install it manually?

##Review
> Having completed this tuorial you should now be able to:

* Install and use **wget** in a Linux Container.

* Install **dmd** and related packages in a Linux Container.

##Next steps.
[Hello World!](./hello_world.md)

##Learn More



