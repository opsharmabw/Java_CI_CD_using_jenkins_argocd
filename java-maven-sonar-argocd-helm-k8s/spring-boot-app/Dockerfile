FROM maven as maven

WORKDIR /usr/src/app
COPY . /usr/src/app

RUN mvn clean package

CMD sleep 3600s

FROM adoptopenjdk/openjdk11:alpine-jre
WORKDIR /opt/app
COPY --from=maven /usr/src/app/target/spring-boot-web.jar app.jar
ENTRYPOINT ["java","-jar","app.jar"]