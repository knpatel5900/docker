# Commamds

      docker container run -dt --name mynginx -v /root/index:/usr/share/nginx/html nginx
      docker container run -dt --name mynginx --mount type=bind,source=/root/index,target=/usr/share/nginx/html nginx
