# webrtc-streamer-docker-compose
spin up the webrtc-streamer project by mpromonet using docker-compose and the prebuilt docker image from dockerhub

for html demo see: https://github.com/mpromonet/webrtc-streamer-html

for the original webrtc-streamer see: https://github.com/mpromonet/webrtc-streamer

# usage of this repo
- spin up the webrtc-streamer with "docker-compose up -d"
- the file config.json is mounted as a volume into the container. to add/remove/edit the video sources, just edit the config.json file in the webrtc-streamer directory of this repo and restart the container. for details about the syntax of config.json see the original project.
- for rtsp-sources with authentication, provide the rtsp url as follows: rtsp://<username>.<password>@<ip-of-webrtc-streamer>/bla/bla (be aware that these are stored in plain text in the config.json, just if you plan to push it to some public place like github ^^)

# access the streams
if the container is up and running, webrtc-streamer provides a demo webserver at http://<ip-of-webrtc-streamer>:8000 where you can check your streams

# access stream in own page
this repo includes a demo html page, which demonstrates how to embed a video stream from webrtc-streamer in html. just edit the webrtc-streamer url in index.html and maybe the video-stream-id before you go.

# note
tested on Raspberry PI 3b with Raspberry PI OS and on Ubuntu 20.04 LTS x86 (only git, docker and docker-compose has to be installed to make this thing work)


thanks to mpromonet for this cool project - all credits regarding webrtc-streamer go to him, I am just the noob who made a simple summary of this huge project for own purposes...
finally there exists a reasonable solution to embed cctv-rtsp urls (and the like) in all the different smart home dashboards (and so on)!
