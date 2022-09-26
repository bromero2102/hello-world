# #EJEMPLO
# FROM openjdk:11-jdk
# ADD build/libs/*.jar app.jar
# ENTRYPOINT [ "java", "-jar", "/app.jar"]

FROM node:8.16 as build-deps
WORKDIR /usr/src/app
COPY package.json yarn.lock ./
RUN yarn
COPY . ./
RUN yarn build