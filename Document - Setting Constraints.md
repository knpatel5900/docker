# Creating Service with Node Label Constraints

    docker service create --name myconstraint --constraint node.labels.region==blr --replicas 3 nginx

# Add a Label to Node:

    docker node update --label-add region=mumbai swarm03

# Running Nodes in Mumbai Region

    docker service create --name myconstraint --constraint node.labels.region==mumbai --replicas 3 nginx
