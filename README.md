# this is tutorial for nginx

This tutorial is followed by:

https://www.youtube.com/watch?v=7VAI73roXaY

## How to run:

move this config file from our project to nginx config folder:

`cp etc/nginx/sites-available/testnginxproject.dev /etc/nginx/sites-available/testnginxproject.dev`

create symlink:

`sudo ln -s /etc/nginx/sites-available/testnginxproject.dev /etc/nginx/sites-enabled/`

run docker compose to create 2 container which mapped to 2 port

`docker compose up -d --build`

now, go to `0.0.0.0:1000` or `0.0.0.0:2000`, you will see the result

check if the config file valid:

`sudo nginx -t`

reload nginx:

`sudo service nginx reload`

read file `nginx/sites-available/testnginxproject.dev` to see the configuration

for api gateway feature, go to `localhost:82/fast-app-no-1` or `localhost:82/fast-app-no-2`, it will redirect to it's related link

## Ability of Nginx

router

redirect

rewrite url

load balancer

api gateway (https://youtu.be/kZV1iVts3Ds?list=UULFCOP-RoCEXCrpDWH12-Nn5w&t=2920)

## Notes:

`try_files` always need to be end by `=404`