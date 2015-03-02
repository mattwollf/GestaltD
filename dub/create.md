#Create a new DUB project.

[GestaltD](../README.md) → [DUB](./README.md) → [create](./create.md)

##Foreword

This tutorial will focus on creating and exploring a new project created with DUB.

DUB provides structure for a new project which makes it easier to manage. 
This structure is rather opinionated, and may create a different workflow than you are used to. 
However, learning this structure is the cost of admission. The end advantage being, that: 

* You have a somewhat standardized project that others (who are also familiar with DUB) can understand 
* You have a tool (DUB) which can streamline your project's workflow.

##Prerequisites
###Required
[Install](./install.md) DUB.

##Core Instruction
### Create a directory to store our projects.
> Here we are going to create a directory called "d_projects" in our home directory. 
> You can rename and move yours wherever you want, but for the purposes of these tutorials, 
> all projects will live in **~/d_projects/** 

    ubuntu@d_virt_env:~ $ mkdir ~/d_projects

> Make **~/d_projects** our **pwd**

    ubuntu@d_virt_env:~ $ cd ~/d_projects

###Create a new DUB project.
> For the purposes of this tutorial we will call our project **hello_dub**. 
> In the future, for other projects, you should give it a name appropriate 
> to the project you are creating.

    ubuntu@d_virt_env:~/d_projects $ dub init hello_dub

> If you see something like the following:

    Successfully created an empty project in '/home/ubuntu/d_projects/hello_dub/'.

> Congratulations, it worked!

##Quick Test
> Successful initialization of a new project should create a directory called **hello_dub**.
> check to see if **~/d_projects/hello_dub** exists.

    ubuntu@d_virt_env:~/d_projects $ ls

> If the directory exists you can now move on to the next step.

##Experimenting
> Move into the **~/d_projects/hello_dub** directory and look around.

    ubuntu@d_virt_env:~ $ cd ~/d_projects/hello_dub

    ubuntu@d_virt_env:~/d_projects/hello_dub $ ls -a

> You should see 2 files and 1 directory.

    dub.json  .gitignore  source

> We will explain these later, but it is good, for now, to be familiar with the 
> files which were created.

> **dub.json** is a configuration file for your project.

> **.gitignore** is a configuration file for git.

> **source** is the directory where your source code is stored.

> Let's look inside **./source**

    ubuntu@d_virt_env:~/d_projects/hello_dub $ cd ./source
    ubuntu@d_virt_env:~/d_projects/hello_dub/source $ ls -a

> There should be 1 file:

    app.d

> This is a minimal scaffolding for a D project.

> We won't do anything with it now, just know where it is.

##RTFM

##Critical Thinking

##Review
> Having completed this tuorial you should now be able to:
* Create a directory do store new DUB projects.
* Initialize a new DUB project which is populated with a minimal application and some configuration files.
* Verify that the project has been created successfully.

##Next steps.
[Run](./run.md) your new project.

##Learn More






