# #EJEMPLO
# FROM openjdk:11-jdk
# ADD build/libs/*.jar app.jar
# ENTRYPOINT [ "java", "-jar", "/app.jar"]

FROM node:6.9.5-alpine
RUN mkdir -p /code
WORKDIR /code
ADD . /code
RUN npm install -g -s --no-progress yarn && \
    yarn && \
    yarn run build && \
    yarn cache clean
CMD [ "npm", "start" ]
EXPOSE 8080