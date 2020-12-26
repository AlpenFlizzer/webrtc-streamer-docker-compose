# webrtc-streamer-docker-compose
spin up the webrtc-streamer project by mpromonet using docker-compose and the prebuilt docker image from dockerhub

for html demo see: https://github.com/mpromonet/webrtc-streamer-html

for the original webrtc-streamer see: https://github.com/mpromonet/webrtc-streamer

# usage of this repo
- spin up the webrtc-streamer with "docker-compose up -d"
- the file config.json is mounted as a volume into the container. to add/remove/edit the video sources, just edit the config.json file in the webrtc-streamer directory of this repo and restart the container. for details about the syntax of config.json see the original project.
- for rtsp-sources (and others) with authentication, for the rtsp url as follows: rtsp://<username>.<password>@<ip>/bla/bla (be aware that these are stored in plain text in the config.json - just if you plan to push it to some public place like github ^^)
