# About

Simple impage that includes databases and tools for data science.

## What you get

- Neo4j with 'APOC' procedures
- Rstudio Server with R and a number of data science packages as well as interfaces to connect to Redshift, Postgresql, MySQL, and Neo4j.
_ Juypter Notebook with Julia, Python 2/3 kernels, as well as R

## Spin up the tools

From within the directory that includes the `docker-compose.yml` file, simply

```
docker-compose up -d
```
which runs the docker in a detached mode.

Check that the containers are running with

```
docker ps
```

Stop the containers with

```
docker-compose Stop
```

And to verify ...

```
docker ps
```

## Note to future self
The volume mappings work from `<host>:<container>`
