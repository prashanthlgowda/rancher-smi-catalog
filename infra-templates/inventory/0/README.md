SMI Server Inventory Microservice

Connects via the IDRAC on a Dell server and collects a comprehensive inventory.

Purpose

The dell-server-inventory container is a stateless spring-boot microservice that exposes a REST API for the purpose of returning a comprehensive JSON formatted inventory of a Dell 11th generation and newer server.

The service can be called without a callback URL in order to run synchronously. If a callback URL is provided in the payload, the service will return immediately and post to the callback URL when the results are available.