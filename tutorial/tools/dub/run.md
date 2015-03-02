#Run a DUB project.

[GestaltD](../README.md) → [DUB](./README.md) → [run](./run.md)

##Foreword

This tutorial will focus on using DUB to build and run projects created in the [previous](./create.md) tutorial.
Here we will only build and run DUB's version of "hello world". 
So, this is a demonstration on using DUB as a tool, building a useful program 
is beyond the scope of this tutorial.

##Prerequisites
###Required
[Create](./create.md) a new DUB project.

##Core Instruction
###Move into your project
> To build and run your project using DUB you need to make the project directory 
> your pwd. Continuing from the previous tutorial on [creating](./create.md) a 
> new dub project, we will be working in **~/d_projects/hello_dub**

    ubuntu@d_virt_env:~ $ cd ~/d_projects/hello_dub

###Build your project
> To build a DUB project you shouldn't use [DMD](/dmd/README.md) as normal. 
> DUB creates and uses configuration files to build a project. 
> It uses DMD in the process of building, compiling and linking all the pieces 
> of your project.

    ubuntu@d_virt_env:~/d_projects/hello_dub $ dub build

> You should get some output similar to this:

    Building hello_dub ~master configuration "application", build type debug.
    Compiling using dmd...
    Linking...

###Check the created files
> Now check to see if we have any new files.

    ubuntu@d_virt_env:~/d_projects/hello_dub $ ls -a

> You should see the same familiar files with some new ones. 
> The only important one we will worry about now is **hello_dub**
> If you can see this file you have completed this tutorial.

##Quick Test
> Run the new executable.

    ubuntu@d_virt_env:~/d_projects/hello_dub $ ./hello_dub

> You should see DUB's version of "hello world" which is:

    Edit source/app.d to start your project.

> Which is basically telling you what to do next, but this is beyond the scope of 
> this tutorial and will be explained in later tutorials. 
> It is good enough, for now, to see this message. 

##Experimenting
If you are inclined, you can edit **~/d_projects/hello_dub/source/app.d** and change 
the application to do something different.

For instance, try changing "Edit source/app.d to start your project." in app.d 
to a custom message of your choice.

##RTFM

##Critical Thinking

##Review
> Having completed this tuorial you should now be able to:
* Build a project created with DUB
* Check to see if the project has been successfully built.
* Execute the binary

##Next steps.

##Learn More






