# CCF API and Specification

A specificaton and set of web service calls to return information about CCF-mapped data

## Development Requirements

* NodeJS v8.11+
* Docker

### Initializing the development environment

After installing the prerequisites, simply run: `npm ci` or `npm instal` to install all dependencies.
Most of the commands necessary embedded in the <package.json> file in the scripts section.

## Some useful commands

### Bundling the schema

`npm run build`

### Validating the schema

`npm run validate`

### Starting a mock server

`npm start` (or `npm run start:mock`)

This will create
a mock OpenAPI server on port 8080 (Try <http://localhost:8080/donors>) and a GraphQL endpoint on port 8081 (Try [http://localhost:8081/graphql](http://localhost:8081/graphql?query=query%20%7B%0A%20%20sample(sampleId%3A%20123)%20%7B%0A%20%20%20%20laterality%0A%20%20%20%20id%0A%20%20%20%20procedure%20%7B%0A%20%20%20%20%20%20id%0A%20%20%20%20%7D%0A%20%20%20%20donor%20%7B%0A%20%20%20%20%20%20id%0A%20%20%20%20%7D%0A%20%20%7D%0A%20%20procedure(procedureId%3A%20123)%20%7B%0A%20%20%20%20id%0A%20%20%20%20donor%20%7B%0A%20%20%20%20%20%20id%0A%20%20%20%20%7D%0A%20%20%7D%0A%20%20samples%20%7B%0A%20%20%20%20id%0A%20%20%20%20procedure%20%7B%0A%20%20%20%20%20%20id%0A%20%20%20%20%20%20donor%20%7B%0A%20%20%20%20%20%20%20%20id%0A%20%20%20%20%20%20%7D%0A%20%20%20%20%7D%0A%20%20%20%20donor%20%7B%0A%20%20%20%20%20%20id%0A%20%20%20%20%7D%0A%20%20%20%20alignment%7B%0A%20%20%20%20%20%20id%0A%20%20%20%20%20%20referenceOrgan%7B%0A%20%20%20%20%20%20%20%20id%0A%20%20%20%20%20%20%20%20imagePath%0A%20%20%20%20%20%20%7D%0A%20%20%20%20%7D%0A%20%20%7D%0A%7D%0A)).

### Starting a mock server with Docker

`docker-compose -f docker/docker-compose.mock-server.yml up` or (`npm run start:docker-mock`)

This will create
a mock OpenAPI server on port 8080 (Try <http://localhost:8080/donors>) and a GraphQL endpoint on port 8081 (Try [http://localhost:8081/graphql](http://localhost:8081/graphql?query=query%20%7B%0A%20%20sample(sampleId%3A%20123)%20%7B%0A%20%20%20%20laterality%0A%20%20%20%20id%0A%20%20%20%20procedure%20%7B%0A%20%20%20%20%20%20id%0A%20%20%20%20%7D%0A%20%20%20%20donor%20%7B%0A%20%20%20%20%20%20id%0A%20%20%20%20%7D%0A%20%20%7D%0A%20%20procedure(procedureId%3A%20123)%20%7B%0A%20%20%20%20id%0A%20%20%20%20donor%20%7B%0A%20%20%20%20%20%20id%0A%20%20%20%20%7D%0A%20%20%7D%0A%20%20samples%20%7B%0A%20%20%20%20id%0A%20%20%20%20procedure%20%7B%0A%20%20%20%20%20%20id%0A%20%20%20%20%20%20donor%20%7B%0A%20%20%20%20%20%20%20%20id%0A%20%20%20%20%20%20%7D%0A%20%20%20%20%7D%0A%20%20%20%20donor%20%7B%0A%20%20%20%20%20%20id%0A%20%20%20%20%7D%0A%20%20%20%20alignment%7B%0A%20%20%20%20%20%20id%0A%20%20%20%20%20%20referenceOrgan%7B%0A%20%20%20%20%20%20%20%20id%0A%20%20%20%20%20%20%20%20imagePath%0A%20%20%20%20%20%20%7D%0A%20%20%20%20%7D%0A%20%20%7D%0A%7D%0A)).
