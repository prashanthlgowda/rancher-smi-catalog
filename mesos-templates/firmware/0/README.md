DellEMC SMI Server Firmware Microservice

Service to compare and apply firmware updates for a Dell server using a repository catalog.

Purpose

For use with Dell 11th Generation and newer servers.

Download the catalog from ftp.dell.com to a local share
Determine updates from a Dell Repository Manager catalog that can be applied to a Dell server
Create a custom catalog
Schedule updates from a Dell Repository Manager catalog to a dell server
Overview

The docker container Exposes a REST API that provides methods to orchestrate the comparison and upgrade Dell 11th Generation and newer servers using a Dell Repository Catalog. The catalog.xml file in the repository contains information about the Update Bundles and their "Dell Update Packages" (DUPs) available in the repository.

By default the dell-server-firmwareupdate docker-container will use the catalog available on ftp.dell.com, unless a custom catalog is specified in the request.

To update firmware, a NFS or CIFS folder with write permission must be mounted on the host, and the local location provided as part of the Docker run command. This share must be accessible by the IDRACs of the Dell servers that you wish to update. When a firmware update is initiated DUPs are stored in a folder this share, and downloaded from there by the IDRAC.

Prerequisites

Docker running on Linux
A NFS or CIFS share running locally or mounted locally on the docker host.
The IDRAC must have read access to the NFS or CIFS host
The IDRAC must be accessible from the Docker Container
Access to ftp.dell.com, or a repository created by the Dell Repository Manager placed on a network share.