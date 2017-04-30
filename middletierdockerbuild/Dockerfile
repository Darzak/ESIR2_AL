FROM java:8
WORKDIR /home/polivier/Documents/AL/ESIR2_AL/middletierdockerbuild
ENV APP_ENV=dev
ADD rss-middletier-0.1.0-SNAPSHOT.jar /rss-middletier-0.1.0-SNAPSHOT.jar
EXPOSE 8080 9191 9192
CMD ["java", "-jar", "/rss-middletier-0.1.0-SNAPSHOT.jar"]
