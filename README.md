# burpsuite Batch deployment for docker

You can boot multiple Burp Suite in the Docker environment

Burp Suite 2020.11.3

Burp Suite(docker iamge)  config addres is :

   /usr/local/docker/burp/space/files/default.json   //You can replace this image in this image to configure Burpsuite


# GUI

Prepare an x11 server <DISPLAY> in x11 ip adders（Xmanager - Passive tool）

```
docker run -di --name burp-gui -e JAVA_OPTS='-Xmx2g ' -e DISPLAY=127.0.0.1:0.0  carpcap/burpsuite-gui:2020.11.3
```






# NO GUI

Suitable for batch deployment on the server, saving the resources of GUI

```
docker run -di --name burp-nogui -e JAVA_OPTS='-Xmx2g '  carpcap/burpsuite:2020.11.3
```



