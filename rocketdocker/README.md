# docker-rocketchat

My `docker-compose.yml` file/setup to run [Rocket.Chat](https://rocket.chat) in production. Optional containers for Hubot and a complete application monitoring stack available as well.

## Installation

1. Make sure you've installed Docker including `docker-compose` support.

2. Create and start up containers using `docker-compose`:

    ```
    docker-compose up -d
    ```
 
### Upgrade to a new Rocket.Chat version

To update your Rocket.Chat server you simply need to make sure the `docker-compose.yml` reflects the version you're trying to update to (\*),  pull the new image from Docker hub, stop and destroy your existing application container and recreate them:

```
git pull
docker-compose up -d rocketchat
```

<sub>_(* I will update this (git tracked) `docker-compose.yml` file according to new Rocket.Chat releases.)_</sub>

### Scaling in case of performance issues

This service file supports the `docker-compose` builtin scaling. For example to add 3 additional application containers you can simply invoke:

```
$ docker-compose up -d --scale rocketchat=4
Starting 185_docker-rocketchat_traefik_1            ... done
Starting 185_docker-rocketchat_mongo_1              ... done
Starting 185_docker-rocketchat_mongo-init-replica_1 ... done
Starting 185_docker-rocketchat_rocketchat_1         ... done
Creating 185_docker-rocketchat_rocketchat_2         ... done
Creating 185_docker-rocketchat_rocketchat_3         ... done
Creating 185_docker-rocketchat_rocketchat_4         ... done
```
  
## Requirements / Dependencies

* Docker

## Version

1.0.0

## License

[MIT](LICENSE)
