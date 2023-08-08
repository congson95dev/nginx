# this is tutorial for nginx

## How to run:

move this config file from our project to nginx config folder:

`cp etc/nginx/sites-available/testnginxproject.dev /etc/nginx/sites-available/testnginxproject.dev`

create symlink:

`sudo ln -s /etc/nginx/sites-available/testnginxproject.dev /etc/nginx/sites-enabled/`

go to `fastapi_simple_app` folder

`cd fastapi_simple_app`

build Dockerfile

`docker build -t fastapi-app .`

create container which mapped to 4 port

`docker run -p 1111:8000 -d fastapi-app`
`docker run -p 2222:8000 -d fastapi-app`
`docker run -p 3333:8000 -d fastapi-app`
`docker run -p 4444:8000 -d fastapi-app`

now, go to `0.0.0.0:1111` or other ports, you will see the result

check if the config file valid:

`sudo nginx -t`

reload nginx:

`sudo service nginx reload`

go to `localhost:82`

read file `nginx/sites-available/testnginxproject.dev` to see the configuration

for load balancer feature, go to `localhost:82/load_balancer`, it will round robin to :1111, :2222 ..

## Ability of Nginx

router

redirect

rewrite url

load balancer

## Notes:

`try_files` always need to be end by `=404`