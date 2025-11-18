# Building a Docker Image

FROM node:18-alpine

WORKDIR /myapp

COPY . .

RUN npm install

CMD ["npm", "run", "dev"]

EXPOSE 3000