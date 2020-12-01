FROM maven:latest
RUN apt-get update
RUN apt-get install git -y
RUN git clone https://github.com/boxfuse/boxfuse-sample-java-war-hello.git
RUN mvn package -f boxfuse-sample-java-war-hello/
CMD cp boxfuse-sample-java-war-hello/target/hello-1.0.war /vol/hello-1.0.war

VOLUME /vol