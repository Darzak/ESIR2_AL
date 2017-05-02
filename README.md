# ESIR2_AL

- Get the sources from github
```
https://github.com/Darzak/ESIR2_AL.git
```

## Step 1 : build docker images

 - Build eureka image
 ```
 cd eurekadockerbuild
 docker build -t myeureka ./
 ```

 - Build middletier image
 ```
 cd ..
 cd middletierdockerbuild
 docker build -t mymiddletier ./
 ```

 - Build edge image
 ```
 cd ..
 cd edgedockerbuild
 docker build -t myedge ./
 ```

 ## Step 2 : run images

 - Run eureka container
 ```
 docker run -p 8080:8080 --name eureka --privileged=true myeureka
 ```
 - Check [eureka service](http://localhost:8080/eureka/)

 - Run middletier container
 ```
docker run -p 9191:9191 --link eureka:eureka -h middletier --name middletier mymiddletier
 ```

 - Run edge container
 ```
 docker run -p 9090:9090 --link eureka:eureka --link middletier:middletier myedge
 ```

 - Check [edge service](http://localhost:9090/jsp/rss.jsp)
