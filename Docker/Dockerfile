FROM openjdk:11
MAINTAINER hillday
RUN mkdir -p /opt/presto-gateway/conf
WORKDIR /opt/presto-gateway
ADD gateway-ha-1.9.0-jar-with-dependencies.jar gateway-ha.jar
ADD gateway-ha-config.yml /opt/presto-gateway/conf/gateway-ha-config.yml
ADD routing_rules.yml /opt/presto-gateway/conf/routing_rules.yml
EXPOSE 8080
ENTRYPOINT ["java", "-jar", "gateway-ha.jar", "server", "conf/gateway-ha-config.yml"]