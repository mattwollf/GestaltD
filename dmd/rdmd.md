#Hello World

[GestaltD](../README.md) → [DMD](./README.md) → [RDMD](./rdmd.md)

##Foreword

The [last](./hello_world.md) tutorial was kind of obligitory. But at least now 
You know how to use **dmd** in it's most basic form.

Now we are going to do something really cool. **rdmd** is THE feature which 
caught my interest in D as a language. Why? Because it spans the gap between D 
as a static language and as a scripting lanugage.

##Prerequisites
###Required
* [Hello World](./hello_world.md)

###Optional

##Core Instruction

> Here we are going to copy our last tutorial and change it just a tiny bit.

    ubuntu@d_virt_env:~$ cd ~/D

> Copy the contents (recursively **-R**) of ./hello_world and make a new directory called ./rdmd

    ubuntu@d_virt_env:~/D$ cp -R ./hello_world ./rdmd

> Move into ./rdmd

    ubuntu@d_virt_env:~/D$ cd ./rdmd

> Delete ./main and ./main.o we don't need them for this tutorial

    ubuntu@d_virt_env:~/D/rdmd$ rm ./main
    ubuntu@d_virt_env:~/D/rdmd$ rm ./main.o

> Now we should only have ./main.d

    ubuntu@d_virt_env:~/D/rdmd$ ls
    main.d

> Now open ./main.d in a text editor

    ubuntu@d_virt_env:~/D/rdmd$ nano ./main.d

> Add only one line of code to the first line of the file.

    #! /usr/bin/rdmd
    import std.stdio;
    void main(){
        writeln("Hello, world");
    }

> The **#!** is called a "shebang". This is a common idiom amongst scripters. 
> basically, it is the purpose is to tell the bash shell that you want to run 
> this file as a script.
> The executable which should Interpretate it is /usr/bin/rdmd

> However, before we can run it, we must change the file's executable flag.

    ubuntu@d_virt_env:~/D/rdmd$ chmod +x ./main.d

> Now we can run ./main.d without compiling it before hand.

    ubuntu@d_virt_env:~/D/rdmd$ ./main.d
    Hello, world

> If you've played with Python, Ruby, etc... This should appeal to you.

> You might notice that the first time running it takes a few seconds to respond. 
> However, it should be very responsive every time after.

> Change the file though. (Just add a space at the end of the file). 
> Run it again and you'll notice it takes a few seconds the first time it is run. 
> But after, it is very responsive again.

> Essentially, the file needs to be re-compiled every time it is changed. 
> But afterwards, it's response time is quicker than any other scripting language. 
> Another benefit is that scripting languages have a very large overhead and require 
> more resources.
> But, as this is compiled into native machine code, we get the benefits of scripting 
> Without the overhead.

##RTFM
    man rdmd
    rdmd --help

##Quick Test
You just did it.

##Experimenting
* If you have the time and experience, make some bench marks comparing D to traditional scripting languages.

##Critical Thinking
* You'll notice that the last tutorial created ./main and ./main.o files. Why doesn't rdmd create these same files?

##Review
> Having completed this tuorial you should now be able to:

* Run D language files as a script.

##Next steps.

##Learn More

