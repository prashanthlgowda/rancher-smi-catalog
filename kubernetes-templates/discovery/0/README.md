SMI Device Discovery Microservices

Purpose

Given an IP Range and credentials, the service attemps to connect to each IP address to try and identify and retrieve basic summary information for all devices within the range. It is written primarily for finding Dell devices, but may identify a few others in the datacenter as well. It is a stateless (12 factor app) that returns a JSON summary response.

This microservice can be used by itself, or as one piece of a larger discovery and inventory effort. This service is used by RackHD as part of a Dell WSMAN discovery and inventory workflow (taskgraph). It is one of several Docker containerized micro-services used as part of the workflow.