# ENV Instruction used in Dockerfile:

    FROM busybox
    ENV NGINX 1.2
    RUN touch web-$NGINX.txt
    CMD ["/bin/sh"]
    
# Using ENV in CLI:

    docker run -dt --name env02 --env USER=ADMINUSER busybox sh

    docker exec -it env02 sh
    echo $USER 
