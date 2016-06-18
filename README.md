LiquidSmooth Source 
----------------------

<img src="https://camo.githubusercontent.com/570ad6c4c10dce1e028d86b02a24e0490d7edb6a/687474703a2f2f73746174732e6c6971756964736d6f6f74682e6e65742f696d616765732f6c6f676f322e706e67">

===================

To get started with LiquidSmooth, you'll need to get
familiar with [Git and Repo](http://source.android.com/source/version-control.html).


Create the Directories
----------------------

You will need to set up some directories in your build environment.

To create them run:

    mkdir -p ~/bin
    mkdir -p ~/liquid

Install the Repository
----------------------

Enter the following to download the "repo" binary:

    curl http://commondatastorage.googleapis.com/git-repo-downloads/repo > ~/bin/repo

    chmod a+x ~/bin/repo

You may need to reboot for these changes to take effect. 
Now enter the following to initialize the repository:

    cd ~/liquid

Repositories:
---------------

Before you continue --> run this in the terminal


    repo init -u git://github.com/LiquidSmooth-Redux/android.git -b mm6.0

    repo sync
    

Building the System
---------------

Build LiquidSmooth with the following command

    ./build-liquid.sh {options} {device}

Use the following as options...
---------------

    Options:
    -c# Cleanin options before build:
            c1 - make liquid
            c2 - make clean
            c3 - make dirty
            c4 - make magic
            c5 - make kernelclean
    -d  Use dex optimizations
    -i  Static Initlogo
    -j# Set jobs
    -s  Sync before build
    -p  Build using pipe
    -o# Select GCC O Level
            Valid O Levels are
            1 (Os) or 3 (O3)
    -z  create build log in 'build-logs'"

Example:
---------------
    ./build-liquid.sh -c3 -p -o3 -j12 hammerhead
    ./build-liquid.sh -c3 -p -o3 -j12 mako
