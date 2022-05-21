FROM ubuntu:latest
COPY . .
ENV PATH /usr/local/go/bin:$PATH
ENV REQUEST_ORIGIN http://localhost:5000
RUN apt-get update && apt-get install -y wget gcc
RUN rm -rf /usr/local/go
RUN wget -c https://golang.org/dl/go1.16.3.linux-amd64.tar.gz
RUN tar -C /usr/local -xzf go1.16.3.linux-amd64.tar.gz
RUN go build
RUN go test
EXPOSE 8080
CMD ./server
