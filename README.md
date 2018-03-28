# Docker EE Agility Demo

See [agility-notes.md](agility-notes.md) for details on what is needed to demo the DTR mirroring features.  The below is the readme for the original demo application and not specific to the agility demo.

# Docker Demo Application
Original Author:  Evan Hazlett (https://github.com/ehazlett/docker-demo)

This is a Go demo application with a PostgreSQL database used for demonstrating Docker and Docker Compose

# Demo

## Requirements

- Install Docker (https://docs.docker.com/installation/)

- Install Docker Compose (https://docs.docker.com/compose/)

## Build

- `docker-compose build`

## Run

- `docker-compose up`

## Cleanup

- `docker-compose down -v --rmi local`
