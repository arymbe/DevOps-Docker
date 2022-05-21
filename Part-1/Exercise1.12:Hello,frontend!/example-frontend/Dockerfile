FROM ubuntu:latest
WORKDIR /usr/src
COPY . .
RUN apt-get update && apt-get install -y curl
RUN curl https://deb.nodesource.com/setup_14.x | apt-get install -y nodejs
RUN apt-get install -y npm
RUN npm install
RUN npm run build
RUN npm install -g serve
CMD ["npx", "serve", "-s", "-l", "5000", "build"]
EXPOSE 5000