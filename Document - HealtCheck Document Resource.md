# Documentation Referred:

https://docs.docker.com/engine/reference/builder/
https://docs.docker.com/engine/reference/run/#healthcheck

# Code Used:

    docker run -dt --name tmp  --health-cmd "curl --fail http://localhost" --health-interval=5s busybox sh
 
    docker run -dt --name tmp2 --health-cmd "curl -f http://localhost" --health-interval=5s --health-retries=1 busybox sh
 
    curl  http://dexter.kplabs.in/test
 
    curl -f http://dexter.kplabs.in/test214.txt
