#FROM arm32v6/openjdk:8-jre-alpine3.8
FROM arm32v6/openjdk:8-jdk-alpine3.8
COPY . /usr/src/myapp
WORKDIR /usr/src/myapp
RUN javac Main.java
CMD ["java", "Main"]