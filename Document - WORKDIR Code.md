# Dockerfile - Demo Code 1:

    FROM busybox
    RUN mkdir -p /root/demo
    WORKDIR /root/demo
    RUN touch file01.txt
    CMD ["/bin/sh"]
    
# Demo Code 2:

    FROM busybox
    RUN mkdir -p /root/demo/context1/context2
    WORKDIR /root/demo
    WORKDIR context1
    WORKDIR context2
    RUN touch file01.txt
    CMD ["/bin/sh"]
