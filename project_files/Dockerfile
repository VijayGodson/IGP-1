FROM ubuntu:22.04
RUN apt-get -y update && apt-get -y upgrade
RUN apt-get -y install openjdk-8-jdk wget
RUN mkdir /usr/local/tomcat
ADD https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.79/bin/apache-tomcat-9.0.79.tar.gz /tmp/apache-tomcat-9.0.79.tar.gz
RUN cd /tmp && tar xvfz apache-tomcat-9.0.79.tar.gz
RUN cp -Rv /tmp/apache-tomcat-9.0.79/* /usr/local/tomcat/
#ADD /var/lib/jenkins/workspace/IGP-1/target/ABCtechnologies-1.0.war /usr/local/tomcat/webapps/
ADD /*.war /usr/local/tomcat/webapps/
EXPOSE 8081
CMD /usr/local/tomcat/bin/catalina.sh run
