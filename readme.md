# Docker and nginx reverse proxy

Demo how to use docker and nginx to setup a reverse proxy.
It uses envsubst in a shell script to replace env variables in the nginx config file

## Use

Set executable bit start.sh

```
chmod +x start.sh
```

Build image with ( use your own tag if you want )

```
docker image build -t yvest/nginx:latest  .
```

And run the container with

```
docker network create mynet
docker container run --network mynet --rm -it  -p 8080:80 yvest/nginx:latest;
```
