# 得到最新的 golang docker 镜像
FROM golang:latest

MAINTAINER cs2mw "wcs2mw@163.com"

# 在容器内部创建一个目录来存储我们的 web 应用，接着使它成为工作目录。
RUN mkdir -p /go/src/helloweb
WORKDIR /go/src/helloweb

# 复制 helloweb 目录到容器中
COPY . /go/src/helloweb

RUN go install -v

RUN ls /go/bin

# 设置 PORT 环境变量
ENV PORT 8080

# 给主机暴露 8080 端口，这样外部网络可以访问你的应用
EXPOSE 8080

# 告诉 Docker 启动容器运行的命令
ENTRYPOINT /go/bin/helloweb