System Management Integration (SMI) Microservices

Introduction

The SMI Microservices are add-on services that are used by rackhd workflows and tasks, primarily focused on adding value for the managemenet of Dell servers. These services use a Zuul gateway and Consul Registry service to present a unified API. Documentation for each service is avialiable on Github in repositories that begin with "smi-service" or on the dockerhub page for the service.

Note: Not all the microservices need to run. You have the option of starting only the ones needed, or manually editing the docker-compose.yml file.