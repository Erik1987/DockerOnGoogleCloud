# DockerOnGoogleCloud

## Initializing docker

// use these commands to set up docker user

$ sudo groupadd docker
$ sudo usermod -aG docker ${USER}
$ su - ${USER}
$ sudo usermod -a -G docker ${USER}


$ docker login -u _json_key -p "$(cat keyfile.json)" https://HOSTNAME
where HOSTNAME is gcr.io, us.gcr.io, eu.gcr.io, or asia.gcr.io.

// push

$ docker push eu.gcr.io/PROJECT_ID/myapp-client:latest
