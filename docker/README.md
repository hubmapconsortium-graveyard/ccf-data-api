# Docker containers for the CCF API

## Mock Server

For development and testing, you can run a mock server using
`docker-compose -f docker-compose.mock-server.yml up`. This will create
a mock OpenAPI server on port 8080 (Try <http://localhost:8080/donors>) and a GraphQL endpoint on port 8081 (Try [http://localhost:8081/graphql](http://localhost:8081/graphql?query=query%20%7B%0A%20%20sample(sampleId%3A%20123)%20%7B%0A%20%20%20%20laterality%0A%20%20%20%20id%0A%20%20%20%20procedure%20%7B%0A%20%20%20%20%20%20id%0A%20%20%20%20%7D%0A%20%20%20%20donor%20%7B%0A%20%20%20%20%20%20id%0A%20%20%20%20%7D%0A%20%20%7D%0A%20%20procedure(procedureId%3A%20123)%20%7B%0A%20%20%20%20id%0A%20%20%20%20donor%20%7B%0A%20%20%20%20%20%20id%0A%20%20%20%20%7D%0A%20%20%7D%0A%20%20samples%20%7B%0A%20%20%20%20id%0A%20%20%20%20procedure%20%7B%0A%20%20%20%20%20%20id%0A%20%20%20%20%20%20donor%20%7B%0A%20%20%20%20%20%20%20%20id%0A%20%20%20%20%20%20%7D%0A%20%20%20%20%7D%0A%20%20%20%20donor%20%7B%0A%20%20%20%20%20%20id%0A%20%20%20%20%7D%0A%20%20%20%20alignment%7B%0A%20%20%20%20%20%20id%0A%20%20%20%20%20%20referenceOrgan%7B%0A%20%20%20%20%20%20%20%20id%0A%20%20%20%20%20%20%20%20imagePath%0A%20%20%20%20%20%20%7D%0A%20%20%20%20%7D%0A%20%20%7D%0A%7D%0A)).
