# this is tutorial for nginx

This tutorial is followed by:

https://www.youtube.com/watch?v=7VAI73roXaY

## How to run:

move this config file from our project to nginx config folder:

`cp etc/nginx/sites-available/testnginxproject.dev /etc/nginx/sites-available/testnginxproject.dev`

create symlink:

`sudo ln -s /etc/nginx/sites-available/testnginxproject.dev /etc/nginx/sites-enabled/`

check if the config file valid:

`sudo nginx -t`

reload nginx:

`sudo service nginx reload`

go to `localhost:82`

read file `nginx/sites-available/testnginxproject.dev` to see the configuration


## Ability of Nginx

router

redirect

rewrite url

load balancer

## Notes:

`try_files` always need to be end by `=404`