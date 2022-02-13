FROM node:16.14.0

WORKDIR /var/www/front

COPY ["./package.json", "./yarn.lock", "./"]

RUN yarn

COPY . ./

RUN ["yarn", "build"]

EXPOSE 3000

CMD [ "yarn", "start" ]