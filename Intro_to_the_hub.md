## Getting started in the Jupyterhub

The purpose of this morning lesson is to get your computational environments set up. We'll be using this hub for the next couple of days.

You all should have received a username and password for the course Hub.  

To sign in, navigate to ***jupyterhub.bigelow.org*** in your browser and enter in your username and password to sign in.

You should now see what looks like a file system on the left, and a working environment on the right.  This is your own personal file system within the larger jupyterhub set up for this course. 


### Setting up your home directory

There are a couple of things we need to do to get your system set up.  First we want to link the storage directory to your home directory.  To do this open up a terminal like this:

1. click the plus in the upper-left corner of the hub
2. under 'Other' select terminal to open up a terminal tab
3. And then type:

```
$ ln -s /mnt/storage/ storage
```

This storage directory contains all of the data for the course as well as space for you to work. Shared course data can be found at:

```
storage/data/
```

Everyone can have their own working directory in the folder 
```
storage/user_lab
```

Let's navigate there now and create working directories for ourselves:

```
$ cd storage/user_lab
$ mkdir {your_username}
```

Feel free to copy data from the data directory into your own directories for you to look at.  Let's try this now.

On the side panel directory navigator, let's navigate into the data directory, open up 'sag_deliverables', and let's open up the AG-910_assembly_stats_updated.csv by double clicking it.  Look through this table, and select a SAG that is more than a million bp in length.  Note the SAG identifier.  I'm going to choose AG-910-B21.

Let's create a destination directory for this data in your terminal session:  
```
$ cd {your_username}
$ mkdir sag_data
```

Copy over the data from the data directory to our working directory:

```
$ cp ~/storage/data/sag_deliverables/AG-910/AG-910-B21.tar.gz sag_data/
```

And then extract information from this target directory: 

```
$ tar -xvf sag_data/AG-910-B21.tar.gz
```

We can navigate into that directory we just extracted using the side browser.  Let's do that right now. You can see all of the files within this deliverables folder. We can look at any of these through the jupyter lab simply by double clicking the file.  

### Conda Environments

The jupyterhub is installed and managed with conda, so all rules for managing and finding conda environments apply within this 'hub.  We have pre-installed several different environments that we'll be using for different lessons throughout this course. To see these environments, type:

```
$ conda env list
```

In addition, some environments are available within jupyter notebooks. To see those environments, open a jupyter notebook session and click on the text in the upper right-hand corner.  You can choose between environments to use. In general, the 'biopy' environment has all the plotting and data analysis packages we'll need for analyzing data within jupyter notebooks. When in doubt, use that environment.

Feel free to install your own environments and software if you want to run your own analyses during the course.  

### Getting data into and out of the 'hub

To upload files, you can either drag-and-drop data from your desktop to your 'hub file system, or you can use the upload up arrow in the upper left-hand portion of your 'hub.  

To download files from the hub to your computer, navigate to the file within the file tree on the left side of the hub, right-click the file and select 'Download'.

