FROM golang:latest

RUN go get github.com/6xiao/go/Common
RUN go get github.com/bitly/go-simplejson
RUN go get github.com/go-sql-driver/mysql
RUN mkdir $GOPATH/src/orderservice

ADD ./orderservice.go $GOPATH/src/orderservice
WORKDIR $GOPATH/src/orderservice
RUN go build .

EXPOSE 8080

ENTRYPOINT ["./orderservice"]
