FROM java:8

RUN mkdir -p /opt /var/zookeeper/data /var/zookeeper/conf \
    && wget -q -O - https://archive.apache.org/dist/zookeeper/zookeeper-3.6.3/apache-zookeeper-3.6.3.tar.gz | tar -xzf - -C /opt \
    && mv /opt/apache-zookeeper-3.6.3 /opt/zookeeper

COPY zoo.cfg /opt/zookeeper/conf/zoo.cfg
WORKDIR /opt/zookeeper

ENTRYPOINT ["/opt/zookeeper/bin/zkServer.sh"]

