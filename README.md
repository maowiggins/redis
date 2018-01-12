# docker-redis

## 快速启动

1、docker run启动

**强烈建议添加 `--privileged` 参数来启用，因为本容器在启动时会有几个内核参数的修改的动作。**

```bash
$ docker run -d --name redis --privileged -p 6379:6379 wiggins/redis:latest
```

2、通过docker-compose来实现快速启动
```bash
$ curl -LkO https://github.com/maowiggins/redis/raw/master/docker-compose.yml
$ docker-compose up -d
```

# 可用变量

| 变量名                       | 变量默认值                     | 说明                                       |
| :------------------------ | ------------------------- | ---------------------------------------- |
| DEFAULT_CONF              | enable                    | 是否试用容器的默认配置文件,值为disable则不生效  |
| REDIS_PASS                | 16位随机生成                   | 当DEFAULT_CONF为非enable值时，此值不生效            |
| CONFIG_FILE               | /etc/redis.conf           | redis配置文件路径                              |

