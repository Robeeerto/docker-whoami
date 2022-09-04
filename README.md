# robeeerto/whoami

使用 Ruby 3.1.2 & Sinatra & Puma

[Docker Hub 網址](https://hub.docker.com/repository/docker/robeeerto/whoami/general)

幫助新手可以釐清 Container 內部的 IP 位置、 HOST 的名稱以及映像檔的環境變數


## 使用方式

```
$ docker image pull robeeerto/whoami # 拉下映像檔

$ docker network create dev # 建立一個虛擬網路

$ docker container run -p 3000:3000 -d --network dev --name whoami-1 robeeerto/whoami # 第一個

$ docker container run -p 3001:3000 -d --network dev --name whoami-2 robeeerto/whoami # 第二個

$ docker container exec -it whoami-1 sh # 進入第一個容器

$ curl whoami-2:3000 # 會得到第二個容器的資訊
```
