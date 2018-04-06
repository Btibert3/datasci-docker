# About

Simple impage that includes databases and tools for data science and maps some of the directories within the containers to your local machine, particularly helpful for debugging and crawling datasets.

## Status

WIP, but things fire up.

## What you get

## Tools

- Neo4j with 'APOC' procedures
- Rstudio Server with R and a number of data science packages as well as interfaces to connect to Redshift, Postgresql, MySQL, and Neo4j.
- Juypter Notebook with Julia, Python 2/3 kernels, as well as R

## Local Directories

I retain the data in

- `~/neo4j`
  -- to store key directories/data that you can use to configure neo4j and access shortcuts for data import
- `~/datasets`
  -- a local file that allows us to share datasets with the containers easily

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
docker-compose stop
```

And to verify ...

```
docker ps
```

## Discussion

The setup makes use of the following images:

- `jupyter/datascience-notebook`
- `btibert3/r-addons` which extends `rocker/hadleyverse` to include a number of R packages on github:  
    - nicolewhite/RNeo4j  
    - stattleship/stattleship-r@helpers

## Note to future self
The volume mappings work from `<host>:<container>`
