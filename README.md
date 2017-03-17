# Dockerized CLJS

Docker image for CLJS projects using [Leiningen](https://leiningen.org/)

## Installation

Add the image to your machine by running the following command:

```
docker pull stankec/dockerized-cljs
```

Alternatively, visit docker.com for more ingormation about this project.

## Configuration

You will have to mount your application into the `/app` directory.

Or if you want to dockerize your application:

```
FROM stankec/dockerized-cljs

COPY . .
RUN lein cljsbuild once min

CMD ["nginx"]
```
