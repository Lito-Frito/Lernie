# Name

Lernie, the multi-headed (container) Hydra for media streaming and management

## Description

This README will guide you through deploying the Lernie multi-container service. The `lernie.yaml` file in this repo is a docker-compose file that will deploy the following services:

* [Plex](https://www.plex.tv/)
* [Sonarr](https://sonarr.tv/)
* [Radarr](https://radarr.video/)
* [Bazarr](https://www.bazarr.media/)
* [Jackett](https://sourceforge.net/projects/jackett.mirror/)
* [Overseer](https://overseerr.dev/)
* [Cloudflare Tunnel](https://www.cloudflare.com/products/tunnel/)

This README assumes you already know what the individual services (e.g. Radarr or Plex) do; to learn what these apps do, go to each service's respective sites to learn more. Also, make sure you change the appropriate lines in the `lernie.yaml` file to reflect your own environment (e.g. volume paths).

## Visuals
#TODO fix this msection


## Installation

You'll need Docker to run the yaml file in this repo. If you don't have Docker installed, you can download it [here](https://www.docker.com/products/docker-desktop).

Once you have Docker installed, you can run the following command in whatever directory the lernie.yaml file lives in order to deploy all the aforementioned services:

```bash
docker-compose -f lernie.yaml up -d
```

It's important to note that the first time you run this command, it will take a while to download the images for each service. Subsequent runs will be much faster. You also need the flag `-d` to run the services in the background.

After you run the command, you can access the services via the following URLs:

* Plex: [http://localhost:32400/web](http://localhost:32400/web)
* Sonarr: [http://localhost:8989](http://localhost:8989)
* Radarr: [http://localhost:7878](http://localhost:7878)
* Bazarr: [http://localhost:6767](http://localhost:6767)
* Jackett: [http://localhost:9117](http://localhost:9117)
* Overseer: [http://localhost:3000](http://localhost:3000)

To stop the services, run the following command:

```bash
docker-compose -f lernie.yaml down
```

If you also want to remove the images, run the following command:

```bash
docker-compose -f lernie.yaml down --rmi all
```

You can think of this command as essentially shutting down the services and then deleting the images.


## Usage
# TODO: Fix this section

The `lernie.yaml` file will set you up with a private media server that you can access from anywhere. You can use the services to manage your media library, download new content, and even find subtitles for your media.

This repo is a proof of concept for how to simulate a private Netflix, via a multi-container service. If you want to run your own private Plex server, it's recommended to use it for media you already own (e.g. ripped from DVDs, Blu-Rays, etc.). 

If you want to use it for pirated content, that's on you. I'm not responsible for what you do with this repo; I'm just trying to get an A on my Docker class project.
