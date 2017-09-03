DellEMC SMI Virtual Network Microservice

A Java Spring Boot Microservice that exposes a REST API, persists network/VLAN settings, and provides IPAM functionality via static IP reservation system.

Introduction

An IPAM micro-service that persists network/VLAN settings, and static IP reservation system.

A docker container for this service is avalable at: https://hub.docker.com/r/rackhd/virtualnetwork/

Purpose

The virtualnetwork (IPAM) Docker container is a spring-boot micro-service that allows a user to define one or more logical virtual networks with associated IPV4 network definitions for later use. It performs basic validation and persists network/VLAN IP configuration data, to include any optional Static IP ranges. The entered data is persisted in a postgres database (linked or attached via settings).

Also provided is API's for reserving and assigning Static IP addresses that may be associated with a network configuration.

To optionally secure the REST endpoints, the micro-service comes compiled with spring-security-oauth2 libraries, and endpoints have pre-defined roles annotated.

The micro-service also serves as a reference implementation for a stand-alone virtualnetwork JAR library (https://github.com/RackHD/smi-lib-virtualnetwork) that can be used independently when writing your own implementation.