# MangaWeb 4 Docker Compose Stack

## Getting Started

By running `$ docker compose up -d`, the stack will be started with default paramters. You can customize further by updating `prod.env` for changing container-specific configuration like OIDC setup etc.

For customizing the compose file itself, including the library path and the HTTP port, you can create a .env file like the following.

```env
DATA_PATH="./data"
HTTP_PORT=8080
```

Alternatively you can specify the variable values via command line parameter directly.

## Running on Portainer

Running on Portainer needs the ability to mount volumes to project file, as we are injecting the `Caddyfile` configuration file to caddy. Unfortunately the *Enable relative path volumes* is only available on the business edition version of Portainer.

This flag needs to be set before deploying the stack, as it can't be set or reset afterward.

Make sure to set the environment variables before running the stack.
