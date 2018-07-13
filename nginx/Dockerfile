#基础镜像
FROM nginx:latest
RUN echo "Asia/shanghai" > /etc/timezone;

RUN rm -rf /etc/localtime;
RUN cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime

#修改配置。
ADD nginx.conf /etc/nginx/



