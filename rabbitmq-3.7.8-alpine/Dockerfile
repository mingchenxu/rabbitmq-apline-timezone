# 基于rabbitmq-alpine，添加时区
FROM rabbitmq:3.7.8-alpine
MAINTAINER xmc <xmc0824@163.com>

# alpine没有时区，这里添加时区
RUN  echo 'http://mirrors.ustc.edu.cn/alpine/v3.8/main' > /etc/apk/repositories \
     && echo 'http://mirrors.ustc.edu.cn/alpine/v3.8/community' >>/etc/apk/repositories \
     && apk update && apk add tzdata \
     && ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime \
     && echo "Asia/Shanghai" > /etc/timezone

