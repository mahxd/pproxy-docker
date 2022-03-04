# Simple and light http/https proxy

Simple docker-compose http/https proxy

Just set environment variables and run docker-compose up -d

## Environmets

.env file contains required variable which are set in proxy command

#### ADDRESS="0.0.0.0"  

#### AUTH="#user:pass"

You can change user and pass value (don't remove starting #)

Or you can disable proxy authentication by commenting AUTH line in .env file

#### HTTP_PORT="55555"

#### HTTPS_PORT="44444"

#### SSL_CERT="/ssl/crt.pem"

Location of cert file

#### SSL_KEY="/ssl/key.pem"

Location of key file

## SSL certificate

if you use ssl certificate for domain xx.yy.zz

ssl certificate should be valid and put under ssl folder with name crt.pem and key.pem or set them on .env file 

then set proxy on your clinet as https://xx.yy.zz:https_port

## Proxy addons

https://chrome.google.com/webstore/detail/proxy-switchyomega/padekgcemlokbadohgkifijomclgjgif?hl=en

https://addons.mozilla.org/en-US/firefox/addon/switchyomega/

## use proxy in shell (bash)

export http_proxy="http://[user:pass@]xx.yy.zz:http_port"

export httpis_proxy="httpis://[user:pass@]xx.yy.zz:https_port"

## command

Command can be changed in docker-compose.yml

Default i set to http only

Just comment default and comment out the one that you want

#### only http proxy

#### http + https Proxy

#### only https proxy

