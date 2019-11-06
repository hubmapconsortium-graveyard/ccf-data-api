# CCF API and Specification

[![GitHub last commit](https://img.shields.io/github/last-commit/hubmapconsortium/ccf-api/master.svg)](https://github.com/hubmapconsortium/ccf-api/commits/master)
[![license](https://img.shields.io/github/license/mashape/apistatus.svg)](LICENSE)
[![View Documentation](https://img.shields.io/badge/documentation-online-brightgreen.svg)](http://smart-api.info/ui/d1f33c1a75e9dcda984194e4d8cea7d8)

A specificaton and set of web service calls to return information about CCF-mapped data

## Specification

The original specification this API is based off of is available on [Google Docs](https://docs.google.com/document/d/1Qgx4mNutE1V3CfQ7y8Lg3rxQy5nhiOSKCSv5MJkPRMc/edit?usp=sharing)

## Documentation

Auto-generated API Documentation is available on [SmartAPI](http://smart-api.info/ui/d1f33c1a75e9dcda984194e4d8cea7d8).

## Development Requirements

* NodeJS v8.11+
* Docker

### Initializing the development environment

After installing the prerequisites, simply run: `npm ci` or `npm install` to install all dependencies.
Most of the commands necessary embedded in the [package.json](package.json) file in the scripts section.

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
