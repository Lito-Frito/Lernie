# Lernie and the River Styx

## Description

This README will explain how to use the files in this repo to create a multi-container media-streaming service. It uses docker-compose to orchestrate the containers. You will need to plug in some values on your own (e.g. Timezone) and provide some environment variables in an `.env` file.

## What This Includes

There are 3 files to launch everything needed for this proof-of-concept: 
* `lernie.yaml`
* `river_styx.yaml`
* `.env`. 

The first will house all the containers/services that handle media (streaming, fetching, etc.). The second will house the Cloudflare Tunnel service as well as an SSH service. The `.env` file will house all the environment variables needed for the services to run properly.

# Getting Started

## Requirements
You'll need: 

* VPN (free ones are usually not ideal)
* a Domain (e.g. my-server.com  ) 
* Docker
* Some comfort with the CLI

## Quick Start
If you have Docker already installed, you already have a `.env` file with the appropriate values, then you can run the following commands to get everything up and running:

```docker compose -f /path/to/lernie.yaml up -d; docker compose -f /path/to/river_styx.yaml up -d```

Docker will then download all the images needed and start the services. 

If you're on Linux and want to save some effort in the future, you can add the following to your `.bash_aliases` or `.bashrc` file:

```alias lernie='docker compose -f /path/to/lernie.yaml up -d'```

```alias river_styx='docker compose -f /path/to/river_styx.yaml up -d'```

Then you can just run `lernie {any command like "up -d" or "restart"}` and `river_styx {some command}` in your terminal to manage the services.

## Starting from Scratch
Clone the repo. Then....
<!-- TODO: Finish this section e.g. create .env file; where to get token values; how to set up CF Tunnels; etc -->



