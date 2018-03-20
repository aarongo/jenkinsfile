FROM edwardregistry.com/devops/java:1.7

MAINTAINER edwardliu

LABEL name="CentOS 7.2.1511 tomcat7"
LABEL vendor="tomcat7"
LABEL license=GPLv2

ADD apache-tomcat-7.0.82 /software/apache-tomcat-7.0.82


RUN rm -rf /software/apache-tomcat-7.0.82/webapps/*

ADD helloworld.war /software/apache-tomcat-7.0.82/webapps/



ENV JAVA_HOME=/software/jdk7
ENV CLASSPATH=.:$JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar
ENV CATALINA_HOME /software/apache-tomcat-7.0.82
ENV CATALINA_BASE /software/apache-tomcat-7.0.82
ENV PATH $PATH:$JAVA_HOME/bin:$CATALINA_HOME/lib:$CATALINA_HOME/bin 
ENV PATH $PATH:$JAVA_HOME/bin

EXPOSE 8080

CMD /software/apache-tomcat-7.0.82/bin/catalina.sh run
