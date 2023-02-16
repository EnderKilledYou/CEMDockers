# docker-openproject
 
## Installation

1. Make sure you've installed Docker including `docker-compose` support.

2. Create and start up containers using `docker-compose`:

    ```
    docker-compose up -d
    ```
 
### Upgrade to a new version

To update your server you simply need to make sure the `docker-compose.yml` reflects the version you're trying to update to (\*),  pull the new image from Docker hub, stop and destroy your existing application container and recreate them:

```
git pull
docker-compose up -d openproject
```

 

 
## Requirements / Dependencies

* Docker

## Version

1.0.0

## License

[MIT](https://opensource.org/license/mit/)
