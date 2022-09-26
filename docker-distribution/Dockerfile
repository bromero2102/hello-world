# #EJEMPLO
# FROM openjdk:11-jdk
# ADD build/libs/*.jar app.jar
# ENTRYPOINT [ "java", "-jar", "/app.jar"]

FROM node:12.18.1
ENV NODE_ENV=production

WORKDIR /app

COPY ["package.json", "package-lock.json*", "./"]

RUN npm install --production

COPY . .

CMD [ "node", "server.js" ]