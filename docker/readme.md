# Commands for Amazon Linux on ec2
```bash
git clone https://github.com/omssp/factorio-docker.git
git checkout build-any-version

sudo docker build --build-arg VERSION=2.0.8 -t factorio .


sudo docker run -d \
  --name factorio_old \
  -p 34197:34197/udp \
  -v ./ffiles:/factorio \
  -e GENERATE_NEW_SAVE=false \
  -e SAVE_NAME=omssp \
  -e DLC_SPACE_AGE=false \
  -e UPDATE_MODS_ON_START=false \
  factorio_old



sudo docker logs --follow factorio_old
sudo docker start factorio_old
sudo docker stop factorio_old 
sudo docker stop factorio_old && sudo docker container rm factorio_old
```


```

sudo docker build --build-arg VERSION=2.0.13 --build-arg SHA256=27b36901a39e593adf28418c0286142c6c7a9f83d156963c7369bd405a25c7d1 -t factorio13 .

sudo docker run -d \
  --name factorio13 \
  -p 34197:34197/udp \
  -v ./ffiles:/factorio \
  -e GENERATE_NEW_SAVE=false \
  -e SAVE_NAME=omssp \
  -e DLC_SPACE_AGE=false \
  -e UPDATE_MODS_ON_START=false \
  factorio13

sudo docker logs --follow factorio13
```

```
sudo docker build --build-arg VERSION=2.0.14 --build-arg SHA256=5a4bc4c3b2a97ed1fc58eb796321e848dcc64435bd91013dd9c78a14a8ce8815 -t factorio14sa .

sudo docker run -d \
  --name factorio14sa \
  -p 34197:34197/udp \
  -v ./ffiles:/factorio \
  -e GENERATE_NEW_SAVE=false \
  -e SAVE_NAME=omssp \
  -e DLC_SPACE_AGE=true \
  -e UPDATE_MODS_ON_START=false \
  factorio14sa

sudo docker logs --follow factorio14sa
```
