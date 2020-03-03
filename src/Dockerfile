FROM node:9.11-alpine

COPY . /app
WORKDIR /app

RUN yarn

EXPOSE 8000

CMD ["yarn", "start"]