FROM ubuntu:16.04
RUN apt update
RUN apt install default-jdk -y
RUN apt install maven -y
RUN apt install tomcat9 -y
RUN apt install git -y
RUN git clone https://github.com/boxfuse/boxfuse-sample-java-war-hello.git
RUN mvn package boxfuse/
RUN cp boxfuse/target/boxfuse.war /var/lib/tomcat9/webapps/
RUN service tomcat9 restart
CMD ["catalina.sh", "start"]