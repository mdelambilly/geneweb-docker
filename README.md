<style>
r { color: Red }
o { color: Orange }
g { color: Green }
b { color: Blue }
</style>

# geneweb-docker

a set of files to host geneweb on a **<r><ins>Synology NAS</r></ins>** in a docker container or as a linux service

## geneweb-run 
contains a docker compose project to create host geneweb in <r><ins>container manager</ins></r>.  
Use the _reverse proxy_ (in _login portal_) to link your URLs to the geneweb ports opened by the compose file.

* create a directory geneweb in the docker shared directory
* copy the directory geneweb-run in it
* create the directory bases in it to match he volume mapping directory
* create container manager project, use the docker/geneweb/geneweb-run directory, use the existing compose file
* build the project
* visit the newly created geneweb daemon at http://_<g>[ip of your NAS]</g>_:2317/

## geneweb-compil
