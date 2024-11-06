# CAMELS-Server Setup

## Introduction

This document describes the setup of the CAMELS-DE server.
- **user**: `camel`, part of the `camel` usergroup with permissions to run docker containers.
- **login** via ssh (your public ssh key has to be added to `/home/camel/.ssh/authorized_keys`).

Code should always be run through docker containers.

## Disks and partitions

There are three disks / partitions configured for this server: **two 500GB SSD hard drives** that are mirroring each other and where the operating system is installed and **one 22 TB HDD drive** that is used mainly to store data and containers that add functionalities to the server and is mounted on `/data`.

## Important directories
- `/home/camel/`: The home folder of the `camels` user. This can be seen as a playground; clone repositories and run containers here. Be aware that the contents of this folder may be removed. For applications/tools that are to be available on the server in the long term, use the `/data/apps` folder.
- `/data/apps/`: Containers / Code that add some sort of long-term functionality to the server should be added here. This could be for example data processing tools that should be available through the server, a website or an API.
- `/data/datasets`: This folder is used to store datasets that can be useful for all users, such as meteorological datasets or a DEM. At some point these datasets should be managed through the `metacatalog-api`.
