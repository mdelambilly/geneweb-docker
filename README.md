# geneweb-docker
a set of files to host geneweb on a Synology NAS
<ul>
    <li>
        geneweb-run: contains a docker compose project to create host geneweb in container manager.<br/>Use the reverse proxy (in login portal) to link your URLs to the geneweb ports opened by the compose file.
        <ul>
            <li>create a diretory geneweb in the docker shared directory</li>
            <li>copy the directory geneweb-run in it</li>
            <li>create the directory bases in it to match he volume mapping directory</li>
            <li>create container manager project, use the docker/geneweb/geneweb-run directory, use the existing compose file</li>
            <li>build the project</li>
            <li>visit the newly created geneweb daemon at http://[ip of your NAS]:2317/
        </ul>
    </li>
</ul>
