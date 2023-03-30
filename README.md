# dhso/cors-anywhere

[![docker build automated](https://img.shields.io/docker/cloud/automated/testcab/cors-anywhere.svg)](https://hub.docker.com/r/dhso/cors-anywhere "dhso/cors-anywhere")
[![](https://images.microbadger.com/badges/image/dhso/cors-anywhere.svg)](https://microbadger.com/images/dhso/cors-anywhere "dhso/cors-anywhere")

The docker image for [cors-anywhere](https://github.com/Rob--W/cors-anywhere).


### Run

```
docker run --rm dhso/cors-anywhere:latest
```

### Envirionment Variables

Env  | Default | Description
---- | ------- | -----------
PORT | 8080    | Server listening port
KEY  |         | Content or filename of TLS Key
CERT |         | Content or filename of TLS Certificate
CORSANYWHERE_BLACKLIST | | If set, requests whose origin is listed are blocked.<br>Comma separated. Example: `https://abuse.example.com,http://abuse.example.com`
CORSANYWHERE_WHITELIST | | If set, requests whose origin is not listed are blocked.<br>If this list is empty, all origins are allowed.<br>Comma separated. Example: `https://good.example.com,http://good.example.com`
CORSANYWHERE_RATELIMIT | | Format: `<max requests per period> <period in minutes> <non-ratelimited hosts>`<br>For example, to blacklist abuse.example.com and rate-limit everything to 50 requests per 3 minutes, except for my.example.com and my2.example.com (which may be unlimited), use:<br>`50 3 my.example.com my2.example.com`
CORSANYWHERE_REQUIREHEADER | | If set, the request must include this header or the API will refuse to proxy. Recommended if you want to prevent users from using the proxy for normal browsing.


## LICENSE

This repository is licensed under [MIT](LICENSE).
