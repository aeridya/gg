# gg - Aeridya Deployment Script

gg is a bash script to assist with deployment of an Aeridya Project

## Description 

gg runs from the project's directory to aid in creating, testing, and deploying a project using Aeridya. 
Requires that a ".prop" file exists in the project directory, this is intended to not be synced in the project remote source (ex: git) as it contains local directory listings.  

**USAGE:** `./gg COMMAND`

Command | Description
--- | ---  
**create** | Creates a new Aeridya project in the current directory.  **WARNING:** Do not use this in an existing project.
**configure** | Creates a new prop file for Aeridya project.  Use this after pulling source from remote
**run** | Runs the Aeridya project.  Works like `go run`, but `go build` the project then runs
**build** | Builds the Aeridya project for production
**install** | Installs the Aeridya project to the machine
**docker** | **TODO:**  Build Aeridya project for Docker
**service** | Creates a service file for systemd based on Aeridya Project
**nginx** | Creates an nginx conf file based on Aeridya Project
**minify** | Minifies CSS and JS files passed in, accepts multiple input files.  Makes new file with extension ".min.js" or ".min.css"
**help** | Shows a help message and exits

### Usage
gg is intended to create and assist with deployment of an Aeridya Project.  Creates the necessary base files for development and contains tools for building.  

#### New Project

To start a new project, create a directory you want to use for the project; the name of the folder will be used as the project name by default.  Then download this gg script in the project directory and make it executable.

```sh
$ curl -f#O https://raw.githubusercontent.com/aeridya/gg/master/gg
$ chmod +x gg
$ ./gg create
```

Now you can go through the prompts to create a new project.

#### Existing Project

gg **REQUIRES** that a `.prop` file exists in the current directory for many of its functions.  It is intended to not be synced with git or other remote code storage options as it contains local configuration settings.  When pulling code from remote storage, you must configure the project.

```sh
$ ./gg configure
```

Once setup is complete, you can use the functions available in gg.
