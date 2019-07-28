# gg - Aeridya Deployment Script

gg is a bash script to assist with deployment of an Aeridya Project

## Description 

gg runs from the project's directory to aid in creating, testing, and deploying a project using Aeridya. 
Requires that a ".prop" file exists in the project directory, this is intended to not be synced in the project remote source (ex: git) as it contains local directory listings.  


## Usage

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
**help** | Shows a help message and exits

