FROM maven:3.9.11-eclipse-temurin-21-noble

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update
RUN apt-get install -y git

RUN mkdir /opt/app
WORKDIR /opt/app
RUN git clone https://github.com/NaRKo101224/prueba_despliegue.git
WORKDIR /opt/app/prueba_despliegue
RUN mvn clean install

EXPOSE 8080

CMD ["java","-jar","target/prueba_despliegue-0.0.1-SNAPSHOT.jar"]
