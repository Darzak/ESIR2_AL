# ESIR2_AL

- Get the sources from github
```
https://github.com/Darzak/ESIR2_AL.git
```

## Step 1 : build docker images

 - Build eureka container
 ```
 cd eurekadockerbuild
 docker build -t myeureka ./
 ```

 - Build middletier container
 ```
 cd ..
 cd middletierdockerbuild
 docker build -t mymiddletier ./
 ```

 - Build edge container
 ```
 cd ..
 cd edgedockerbuild
 docker build -t myedge ./
 ```
