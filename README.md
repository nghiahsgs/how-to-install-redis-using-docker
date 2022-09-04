# how-to-install-redis-using-docker
how to install redis using docker


## step 1: install docker 
```
https://nghiahsgs.com/cai-dat-va-su-dung-docker-co-ban-tren-ubuntu-server/
```

## step 2: install and run the container
```
docker run --name my-redis -p 6379:6379 -d redis
```

```
docker images
docker ps
```

## Step 3

go to inside container
```
docker exec -it my-redis sh
redis-cli

```

set password for redis
```
redis 127.0.0.1:6379> AUTH PASSWORD
(error) ERR Client sent AUTH, but no password is set
redis 127.0.0.1:6379> CONFIG SET requirepass "mypass"
OK
redis 127.0.0.1:6379> AUTH mypass
Ok
```

exit container and connect redis like normally. If you want to connect redis remotely, simple, ufw allow port for redis 6379

