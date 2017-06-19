# logstash-docker
Dockerfile and configuration files for logstash

This docker file pulls from the official elastic docker image repository and adds a few changes. The current elastic version for all of their docker images is 5.4.1. Please install elasticsearch from our other repository before attempting this install! 

After cloning this repository into an empty directory, cd into the new directory and issue the following command:
```
$ sudo docker build -t logstash .
```
Then run the container by using the following:
```
$ sudo docker run --name logstash -d --net elk --ip 172.18.0.3 logstash
```

*Note: this IP address is critical for the rest of the elk suite to function, as our build relies on specific IP's for containers to communicate.

For more information and references on settings, configuration, and runtime commands, check out https://www.elastic.co/guide/en/logstash/current/_pulling_the_image.html for the official elastic documentation. 
