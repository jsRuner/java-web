FROM tomcat:latest

#作者
MAINTAINER hiwower <hiwower@gmail.com>

#定义工作目录
ENV WORK_PATH /usr/local/tomcat/conf

#定义要替换的文件名
ENV USER_CONF_FILE_NAME tomcat-users.xml

#定义要替换的server.xml文件名
ENV SERVER_CONF_FILE_NAME server.xml

#删除原文件tomcat-users.xml
RUN rm $WORK_PATH/$USER_CONF_FILE_NAME

#复制文件tomcat-users.xml
COPY  ./$USER_CONF_FILE_NAME $WORK_PATH/

#删除原文件server.xml
RUN rm $WORK_PATH/$SERVER_CONF_FILE_NAME

#复制文件server.xml
COPY  ./$SERVER_CONF_FILE_NAME $WORK_PATH/