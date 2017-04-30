FROM java:7

RUN apt-get update && apt-get install -y git wget libgradle-core-java

RUN git clone https://github.com/Netflix/recipes-rss.git

WORKDIR /recipes-rss
ENV APP_ENV=dev
RUN ./gradlew clean build

EXPOSE 8080 9191 9192

WORKDIR /recipes-rss
CMD ["java", "-jar", "/rss-edge/build/libs/rss-edge-0.1.0-SNAPSHOT.jar"]
