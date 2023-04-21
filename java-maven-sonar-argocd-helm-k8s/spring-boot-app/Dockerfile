FROM maven:3.6.3 as maven

WORKDIR /usr/src/app
COPY . /usr/src/app

RUN cd java-maven-sonar-argocd-helm-k8s/spring-boot-app/ && mvn clean package

CMD sleep 3600s