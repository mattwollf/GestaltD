#Install DUB.

[GestaltD](../README.md) → [DUB](./README.md) → [install](./install.md)

##Foreword

This tutorial will focus exclusively on installing DUB onto your virtual environment.

##Prerequisites
###Required
* Install [git](/git/README.md)

###Optional
* Create a [LXC](/lxc/README.md) virtual environment.

##Core Instruction
###Download DUB
> Create a convenient place to store the files.

    ubuntu@d_virt_env:~ $ mkdir ~/git

    ubuntu@d_virt_env:~ $ cd ~/git

> Download the official source code from github.

    ubuntu@d_virt_env:~/git $ git clone https://github.com/D-Programming-Language/dub.git

> Move into the DUB project directory.

    ubuntu@d_virt_env:~/git $ cd ./dub

###Compile DUB from source.
> Install libcurl3 as a pre-requisit to compile DUB

    ubuntu@d_virt_env:~/git/dub $ sudo apt-get install libcurl3-dev

> Start the build process.

    ubuntu@d_virt_env:~/git/dub $ ./build.sh

###Move the executable to /usr/local/bin
> Move the new executable into /usr/local/bin so it will be recognized as 
> a universal command.

    ubuntu@d_virt_env:~/git/dub $ sudo cp ./bin/dub /usr/local/bin/dub

###Finish
> DUB should be installed now.

##Quick Test
> All we are doing here is verifying that dub has been installed.

    ubuntu@d_virt_env:~ $ dub -h

> All this should do is print out the options for dub. 
> If you get something else you failed on some step.

##Experimenting
> There isn't much to experiment with at this stage. 
> Move on to the next stage.

##RTFM

##Critical Thinking

##Review
> Having completed this tuorial you should now be able to:
* Download DUB from GitHub.
* Compile DUB from source.
* Install the binaries to /usr/local/bin
* Verify that it has installed.

##Next steps.
[Create](./create.md) a new DUB project.

##Learn More






