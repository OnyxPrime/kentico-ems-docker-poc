This repo provides a docker-compose file configured to create a local Kentico 12 environment. 

## Pre-requisites
- Download and install [Docker Desktop](https://docs.docker.com/get-started).
- Clone, or copy, the [Docker compose file](https://github.com/OnyxPrime/kentico-ems-docker-poc/blob/master/docker-compose.yml) we'll use to create the Kentico EMS environment.

## Getting Started

- Ensure Docker Desktop is setup to run Windows containers.
- From a command-line,
    - switch to the directory containing the cloned .yml file from above
    -  run `docker-compose up`
- Navigate
    - Dancing Goat site http://localhost:60051/Kentico12_Admin
    - Admin site http://localhost:60051/Kentico12_Admin
        - username: administrator
        - password: _none_ 
- To shutdown the environment, press CTRL + C

_Note: The current setup uses a trial license which expires 14 days from the docker image creation (10/25/2019). To obtain a new trial license key, navigate to https://www.kentico.com/download-demo/trial-license-key and fill out the form._

## Configuration
This solution uses 2 custom Windows based images.

1. IIS image hosting the web applications with Kentico EMS installed
2. SQL Server image with a Kentico DB.
    - server name: localhost, 1435
    - username: sa
    - password: Pass@word1 
