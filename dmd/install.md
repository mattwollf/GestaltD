#Installing the D compiler DMD

##Foreword



##Prerequisites
###Required
* Ubuntu

###Optional
* An LXC container

    #the default username : password is ubuntu : ubuntu
    sudo passwd <enter your new password>   #Optional: change the password
    
    sudo apt-get install wget   #wget is a simplistic http client. All it does is download a file (see usage below)
    
    cd ~    #Move to home directory
    mkdir ./Downloads   #create a folder for downloads if it doesn't exist
    cd ./Downloads  #make downloads your pwd
    
    wget http://downloads.dlang.org/releases/2014/dmd_2.066.1-0_amd64.deb   #download the latest binary. You may need to choose another binary depending on your situation
    sudo dpkg -i ./dmd_2.066.1-0_amd64.deb  #install the D compiler
    sudo apt-get -f install #install dmd's dependencies
    
    sudo apt-get install nano   #optional: nano is a simplistic text editor
    
        #----begin ~/d/hello/hello.d--------------------------------------------
        #! /usr/bin/rdmd
        
        import std.stdio;
        
        void main(){
            writeln("Hello, world");
        }
        #----end ~/d/hello/hello.d----------------------------------------------