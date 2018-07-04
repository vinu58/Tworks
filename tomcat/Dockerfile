FROM alpine
RUN apk upgrade
RUN apk --update add openjdk7-jre
ADD ./tomcat /opt/tomcat
ENV Default: JAVA_OPTS: -Djava.awt.headless=true -XX:+UseG1GC -Dfile.encoding=UTF-8
ENV default: TOMCAT_HTTP_PORT_NUMBER:8080
ENV default: TOMCAT_AJP_PORT_NUMBER: 8009
ENV default: JAVA_HOME: /usr/lib/jvm/java-1.7-openjdk/
ENV default: TOMCAT_HOME: /opt/tomcat
CMD /opt/tomcat/bin/catalina.sh run
EXPOSE 8080
