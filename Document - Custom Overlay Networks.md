# Create Service with Custom Overlay Network:

    docker service create --name myoverlay --network mynetwork --replicas 3 nginx

# Verify Networks:

     docker network ls

# Find the IP of Container

    docker container inspect [CONTAINER-NAME]

# Connect to Container and Install Ping

    docker container exec -it [CONTAINER-NAME]
    apt-get update && apt-get install iputils-ping
    ping [IP]

