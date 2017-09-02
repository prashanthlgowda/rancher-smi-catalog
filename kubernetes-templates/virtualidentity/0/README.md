DellEMC SMI Virtual Identity Microservice

A virtual identity (MAC,IQN,WWN) generation and reservation system.

A docker container for this service is avalable at: https://hub.docker.com/r/rackhd/virtualidentity/

Purpose

The Virtual Identity docker container runs a spring-boot micro-service that exposes a REST API for a user or application to reserve and assign virtual identities (MAC Addresses, IQN's, WWN's).

This code generates a default global pools for MAC addresses on startup using a pre-defined starting pattern.
A user can create their own pool with their own starting pattern if desired and use it. Pools can be expanded at a later date. Pools can exist for MAC addresses, IQN’s, and WWN’s.

A user has the ability to “Reserve” a quantity of virtual identities from a pool for a UsageID (can be a generic identifier for the process or a specific system identifier) from any of the virtual pools.

The typical use-case is to reserve the expected quantity of virtual identities from a pool for a workflow as part of a two-phase process (reservation then assignment). The two phase process insures the total quantity is available for the whole process.

Reserved virtual identities can expire and be reclaimed if not released or assigned within a time limit. A user can “Assign” one or more virtual Identities from a pool to a specific usage Id for the device where it is actually used.

A user can “Release” a virtual identity back to the pool if it is no longer needed. Additionally, the option to release all of the virtual identities for a specific usage ID is provided.