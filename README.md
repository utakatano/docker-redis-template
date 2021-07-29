# Redis Template with Docker/Docker Compose

This is Redis template that you can run though you don't install Redis in your local machine.

## Environment

- [Redis](https://redis.io) ... 6.2.5

## How to run local development

1. Please run docker container with `docker-compose up` command,  
then you need to access it with `docker-compose exec`.

```sh
% docker-compose up -d --build
% docker-compose exec redis bash
```

2. In the docker container, `redis-cli` can interact with the Redis server. 

```sh
root@84fb667b80f0:/＃ redis-cli
127.0.0.1:6379> 
127.0.0.1:6379> 
127.0.0.1:6379> keys *
(empty array)
127.0.0.1:6379> ping
PONG
127.0.0.1:6379> set test "Hello, World!!"
OK
127.0.0.1:6379> get test
"Hello, World!!"
127.0.0.1:6379> INFO
# Server
redis_version:6.2.5
redis_git_sha1:00000000
redis_git_dirty:0
redis_build_id:38e65183e5f5784b
redis_mode:standalone
os:Linux 5.10.25-linuxkit aarch64
arch_bits:64
...
```
