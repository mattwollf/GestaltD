#Installing a D virtual environment using lxc on your Ubuntu host

##Foreword

Installation of Linux containers is pretty straight forward. Everything required is availible in Ubuntu's apt repository.

##Prerequisites

* Install Ubuntu.

* Your user must have **sudo** privileges.

## Instruction

> The First thing you want to do is install **lxc** from the apt repository

    user@host ~ $sudo apt-get install lxc lxc-templates

>*This will install **lxc** along with some generic templates. 
>Included in the lxc-templates package is the "ubuntu" template, which is what we will use for each tutorial.*

    user@host ~ $sudo lxc-create -t ubuntu -n d_virt_env

>*Create a container named **d_virt_env** from the **ubuntu** template.*

>>Notice there are two flags:
>>>**-n** This is the name of your container.
>>>**-t** This is the container template you want to use.

>*You don't need to call your container **d_virt_env**, you can name it whatever you want. However, for the purposes of this tutorial we will call it **d_virt_env** because this tutorial is about the D environment.*

    user@host ~ $sudo lxc-start -n d_virt_env

>*Start your D virtual environment (**d_virt_env**)*

    user@host ~ $sudo lxc-info -n d_virt_env

>*Get **d_virt_env**'s info*

>*Notice the **IP Address** you can use this to log into the container at any time.*

    user@host ~ $ssh ubuntu@<IP Address>

>*Log into the **d_virt_env** container as if it were an individual machine*

>*The default username is **ubuntu***

>*The default password is: **ubuntu***

## Next steps.
* Install the DMD compiler

## Learn More