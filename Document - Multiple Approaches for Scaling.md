# Two Approaches:

    docker service scale service01=1
    docker service update --replicas 1 service02

# Scaling Multiple Services Together:

    docker service scale service01=3 service02=3
