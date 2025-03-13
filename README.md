$\color{Apricot}{The\ quick\ brown\ fox\ jumps\ over\ the\ lazy\ dog.}$

# geneweb-docker

a set of files to host geneweb on a **$\color{red}{Synology\ NAS}$** in a docker container or as a linux service

## geneweb-run 
contains a docker compose project to create host geneweb in _<ins>container manager</ins>_.  
Use the _reverse proxy_ (in _login portal_) to link your URLs to the geneweb ports opened by the compose file.

* create a directory geneweb in the docker shared directory
* copy the directory geneweb-run in it
* create the directory bases in it to match he volume mapping directory
* create container manager project, use the docker/geneweb/geneweb-run directory, use the existing compose file
* customize arguments in the compose file in container manager and build the project
* visit the newly created geneweb daemon at http:// $\color{green}{\<ip\ of\ your\ NAS\>}$ :2317
* create a reversy proxy rule if needed

## geneweb-compil
