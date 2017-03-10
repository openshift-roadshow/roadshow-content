# Prepackaged OpenShift Roadshow content

OpenShift Roadshow content packaged as a self-container Docker image that can
be run on OpenShift or on any Docker installation.

## Usage with Docker

With plain docker installation, just run the container

```
docker run -ti -p 8080:8080 docker.io/mjelen/roadshow-content
```

and open `http://localhost:8080/`.

## Usage with OpenShift

Simply deploy the image on OpenShift and expose route to access the content

```
oc new-app docker.io/mjelen/roadshow-content --name roadshow
oc expose svc roadshow
```

open the generated URL in your browser of choice.
