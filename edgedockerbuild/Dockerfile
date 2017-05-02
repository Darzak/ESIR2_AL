FROM java:7

RUN apt-get update && apt-get install -y git wget libgradle-core-java

RUN git clone https://github.com/Netflix/recipes-rss.git
COPY edge.properties /recipes-rss/rss-edge/src/main/resources/edge.properties

WORKDIR /recipes-rss
ENV APP_ENV=dev
RUN ./gradlew clean build

WORKDIR /recipes-rss
CMD ["java", "-jar", "rss-edge/build/libs/rss-edge-0.1.0-SNAPSHOT.jar"]
