FROM ubuntu:16.04
RUN apt-get update
RUN apt-get update && apt-get install -y \
  default-jre \
  default-jdk \
  git \
  maven
RUN mvn -version
RUN mkdir -p $HOME/SpringbootWebapp
WORKDIR $HOME/SpringbootWebapp
COPY pom.xml .
RUN mvn dependency:go-offline
COPY src/ src/
RUN mvn package
ENTRYPOINT ["java", "-jar", "target/HLSpringBootWeb-1.0-SNAPSHOT.jar"]
