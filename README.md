# Docker Nginx RTMP

This Dockerfile uses `nginx-rtmp-module`. Server receives RTMP streams and publish HLS.
Note that this publishes only one resolution on HLS.

## How to use

#### 1. Build the Dockerfile


```sh
docker build -t nginx_rtmp .
```

#### 2. run the Container

```sh
docker run -t -i -p 1935:1935 -p 80:80 --rm nginx_rtmp
```

#### 3. send RTMP stream from client

send stream to `rtmp://ip-address:1935/live/stream_name`. 
you can also receive RTMP stream with the same url.

#### 4. play hls

media playlist is `http://ip-address:8080/hls/stream_name.m3u8`


