FROM node:14-alpine
LABEL Author Carmine DiMascio <cdimascio@gmail.com>

RUN mkdir -p /usr/src/build
WORKDIR /usr/src/build

COPY ["package.json", "package-lock.json*", "/usr/src/build/"]
RUN npm install

COPY . /usr/src/build
RUN npm run compile

EXPOSE 3000

CMD [ "npm", "start" ]
