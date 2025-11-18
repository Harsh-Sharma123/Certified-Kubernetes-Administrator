# Building docker image in stages (Multi-Stage Build)

FROM node:18-alpine AS installer
WORKDIR /myapp
COPY package*.json .
RUN npm install
COPY . .
RUN npm run build 

FROM nginx:latest AS deployer
COPY --from=installer /myapp/build /usr/share/nginx/html