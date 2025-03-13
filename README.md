# geneweb-docker

a set of files to host geneweb on a **$\color{red}{Synology\ NAS}$** in a docker container or as a linux service

<details>
 <summary><b><ins>geneweb-run:</ins></b> Install geneweb as a docker application with <i>Container Manager</i></summary>

### first deployment
1. create a directory geneweb in the docker shared directory
2. copy the directory geneweb-run in it
3. create the directory bases in it to match he volume mapping directory
4. create container manager project, use the docker/geneweb/geneweb-run directory, use the existing compose file
5. customize arguments in the compose file in container manager and build the project
6. visit the newly created geneweb daemon at http:// $\color{green}{\<ip\ of\ your\ NAS\>}$ :2317
7. create a reversy proxy rule if needed

### next deployment
1. stop the project in container manager. This will stop the geneweb-run container.
2. clean the project in container manager. This will delete the geneweb-run container.
3. delete the geneweb-run image in container manager
4. build the project

Deployments can be sped up the  by pulling those two images:
- ocaml/opam:debian-12-ocaml-4.14
- debian:12-slim

this can be done in Container Manager app or by using the following docker command line with the Task Scheduler
```
docker pull ocaml/opam:debian-12-ocaml-4.14
```
```
docker pull debian:12-slim
```

</details>

<details>
 <summary><b><ins>geneweb-compil:</ins></b> creates a docker container to compile geneweb and a script to deploy the service</summary>

 \
 contains a docker compose project to create a container to build geneweb executable compatible with Synology DSM 7 and above
</details>

<details>
  <summary>Interesting links</summary>

-  Markdown
    - [github doc](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
    - [Markdown Editor](https://binarytree.dev/markdown/me)
    - [Table Of Content](https://binarytree.dev/markdown/toc)
    - [Markdown Table Generator](https://binarytree.dev/markdown/md_table_generator)
    - [Cheatsheet](https://github.com/lifeparticle/Markdown-Cheatsheet/)
    - [Emoji](https://gist.github.com/rxaviers/7360908)
- NAS Security
    - [Protec your NAS in english](https://mariushosting.com/how-to-protect-and-secure-your-synology-nas-from-attacks/)
    - [Secure your NAS in french](https://news.infomaniak.com/10-methodes-pour-securiser-lacces-de-votre-nas-synology/)
</details>

