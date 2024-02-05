## Run development environment

Required: \
Docker

### Setup

Set ```.env.dev``` vars

### Run compose
```
$ docker compose -f compose.yaml -f compose-dev.yaml up
```

### Expected result
After the application starts, navigate to `http://localhost:80` in your web browser

## Run in production
Required: \
Docker \
NGINX

Set production .env vars

### Use docker contexts to deploy:
```
$ docker context create --docker "host=ssh://deployer@mydomain.test" prod
$ docker context use prod
$ docker compose up --build
```
### Expected Result 
After the application starts, navigate to `http://mydomain.test` in your web browser