FROM tomcat:7

ENV EUREKA_VERSION 1.1.158

RUN apt-get update && apt-get install -y wget git
WORKDIR /
RUN wget http://repo1.maven.org/maven2/com/netflix/eureka/eureka-server/${EUREKA_VERSION}/eureka-server-${EUREKA_VERSION}.war
RUN cp /eureka-server-${EUREKA_VERSION}.war /usr/local/tomcat/webapps/eureka.war
