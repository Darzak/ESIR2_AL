FROM java:7

RUN apt-get update && apt-get install -y git libgradle-core-java

RUN git clone https://github.com/Netflix/recipes-rss.git

COPY middletier.properties /recipes-rss/rss-middletier/src/main/resources/middletier.properties

WORKDIR /recipes-rss
ENV APP_ENV=dev
RUN ./gradlew clean build

CMD ["java", "-jar", "rss-middletier/build/libs/rss-middletier-0.1.0-SNAPSHOT.jar"]
