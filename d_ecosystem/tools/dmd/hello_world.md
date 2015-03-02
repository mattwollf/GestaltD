#Hello World

[GestaltD](../README.md) → [DMD](./README.md) → [Hello World](./hello_world.md)

##Foreword

So, here we are, the obligitory "Hello World". She's not sexy, but I'll be 
damned if she doesn't get the job done.

##Prerequisites
###Required
* [Install](./install.md) DMD

###Optional

##Core Instruction
> OK, first things first. We need a project directory to put our code.

    ubuntu@d_virt_env:~$ mkdir ~/D
    ubuntu@d_virt_env:~$ mkdir ~/D/hello_world/

> Move into our project directory

    ubuntu@d_virt_env:~$ cd ~/D/hello_world/

> create a new file with **touch** 
> (FYI **touch** is **supposed** to update the time stamp of a file 
> But, if that file doesn't exist it creates it outright, which is convenient. (Seriously, RTFM)) 

    ubuntu@d_virt_env:~/D/hello_world/$ touch ./main.d

> Now we need a way to edit ./main.d However, if you are using a Linux container, 
> You shouldn't be suprised by now to know that one isn't installed by default.

> This isn't a tutorial on text editors, so I'll let you decide what you want to use.
> EMACS, VIM, I don't give a damn. I'm going to use **nano** while and get the job 
> done before text editor the holy war is finished.

> If you don't know how to use **nano** RTFM.

    ubuntu@d_virt_env:~/D/hello_world/$ sudo apt-get install nano

> Open ./main.d

    ubuntu@d_virt_env:~/D/hello_world/$ nano ./main.d

> Copy this text and save.

    import std.stdio;
    void main(){
        writeln("Hello, world");
    }

> I'm not going to spend any time explaining what this does. This tutorial is 
> focusing on the dmd compiler, not D code itself. I'll just say this...
> If you don't know what "Hello World" does, you are in the wrong tutorial.

> I will however give one last clue for users who might not know how to save a 
> file in nano. (Last hint on text editors, I swear)

    <ctrl>+x

> exits nano.

> If your buffer has been edited, (Your file is unsaved), you will be prompted to save.

> press "y" then (for "yes")

    <enter>

> Compile time! Now we can party!

    ubuntu@d_virt_env:~/D/hello_world/$ dmd ./main.d

###Hello World Successfully Compiled
> If you entered the above code in correctly, you should get no response. 
> This is normal.

> We can check if it worked though:

    ubuntu@d_virt_env:~/D/hello_world/$ ls
    main  main.d  main.o

> If everything worked out we should see 2 new files ./main and ./main.o

> Ignore ./main.o for now. It's beyond our pay grade for this tutorial.

> However, ./main is the money maker

> We can execute it like this:

    ubuntu@d_virt_env:~/D/hello_world/$ ./main
    Hello, world

> If you see "Hello, world", congratulations. Mission accomplished!

###Hello World Didn't Successfully Compile
> If you get output like this:

    ./main.d(4): Error: found '}' when expecting ';' following statement

> You likely typed the code in wrong. Common mistakes are missing semi-colons **;** 
> or curly brackets **}**.

> Here the compiler is giving you a hint that the error is on line 4 **./main.d(4)** 
> and the code is expecting a semi-colon **;**

> Go back and make sure the code is correct.

##RTFM
> If you are new to editing on a command line you might want to learn more 
> about text editors.

    ubuntu@d_virt_env:~$ man nano
    ubuntu@d_virt_env:~$ nano --help

> We will dive into **dmd** in greater detail in the following tutorials. 
> But it doesn't hurt to RTFM now.

##Quick Test
> If you successfully compiled ./main.d that was the "quick test"

##Experimenting
> This isn't a tutorial on the D language. But that shouldn't stop you from 
> playing around if you want to [learn](http://wiki.dlang.org/Getting_Started).

##Critical Thinking
* So... about that **./main.o**, What is that anyway?

##Review
> Having completed this tuorial you should now be able to:

* Create a project directory.

* Create a ./main.d file.

* Open ./main.d in a text editor.

* Save the file with some code in it.

* Compile the code.

* Output some text to the screen.

* If this is a first for you... No, you are not a programmer yet.

##Next steps.
[RDMD](./rdmd.md)

##Learn More
[Getting Started](http://wiki.dlang.org/Getting_Started) Dlang Wiki

