# 环境
# 1. docker (https://docs.docker.com/install/)
# 2. docker-compose (https://docs.docker.com/compose/install/)

# 开启
$ docker-compose up -d
# 关闭
$ docker-compose stop

# 目录结构：
  ├─mysql
  ├─nginx
  │  └─sites    站点配置目录，添加站点需要增加对应配置
  ├─php
  └─www         站点目录，可以链接站点到该目录下

# 挂载日志
$ docker-compose logs -f [服务名]

# 项目安装
$ docker run --rm --interactive --tty \
 --volume $PWD:/app \
 --workdir /app \
 composer install --ignore-platform-reqs --no-scripts
$ docker-compose exec php-fpm bash

