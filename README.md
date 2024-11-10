# Name

Lernie, the multi-headed (container) Hydra for media streaming and management

## Description

This repo has all the necessary files to build a multi-container media-streaming service. It uses docker-compose to orchestrate the containers. The containers are:

* Plex
* Sonarr
* Radarr
* Bazarr
* Jackett
* Overseer
* Cloudflare Tunnel

Here's a quick rundown of what each container does:

* Plex: Media server (sort of like your own private Netflix
* Sonarr: Tracks TV shows you flag for monitoring and talks to your indexers outlined in Jackett
* Radarr: Same as Sonarr but for movies
* Bazarr: Finds subtitles for your media
* Jackett: Indexer aggregator
* Overseer: Allows others to make requests, submit issues, and other features on your media libraries
* Cloudflare Tunnel: Creates a tunnel to route whatever traffic you want to the outside world (as opposed to opening ports on your router/firewall 😬), sort of like a VPN but with less hassle

This README will only explain what's available in this repo. For more detailed information on each container, please refer to the READMEs in the folders nested within.

## Visuals

#TODO fix this section
Probs include some gifs or carosel of images showing the services in action

## Installation

You will need [Docker](https://docs.docker.com/engine/install/) in order to make use of the config files found within this repo. You could always run these services as stand alone apps but it's always best to treat your infra as cattle, not pets (i.e. make them modular and disposable, not precious and irreplaceable). If you can't use Docker (e.g. on Synology or Windows), you can still mostly follow the principles outlined in this repo but I recommend looking up tutorials on how to set up each service with your contrainsts/environment.

## Usage

This repo is a proof of concept for how to simulate a private Netflix, via a multi-container service. If you want to run your own private Plex server, it's recommended to use it for media you already own (i.e. ripped from DVDs, Blu-Rays, etc.). 

If you want to use it for pirated content, that's on you. I'm not responsible for what you do with this repo; I'm just trying to get an A on my Docker class project.

## Support

Please feel free to open any issues for bugs or feature requests. I'll also gladly accept pull requests if you want to contribute to this project.

### How to Contribute

## Roadmap

Eventually, this proof of concept will include services like Emby or Jellyfin, as well as a VPN service to ensure your traffic is secure (in case you're sharing access but don't want to expose your geolocation).

## Contributing

As mentioned, I'd greatly welcome any contributions to this project. Please feel free to open an issue or submit a pull request.

## Authors and acknowledgment

Shoutout to the people who made these apps and containers; you are the real MVPs, not the SaaS you make haha. 

## License

This project is licensed under the MIT license. Please see the LICENSE file for more information.

## Project status

This is passively being worked on. I'm not actively developing this project, but I will accept pull requests and issues as they come in.

```
