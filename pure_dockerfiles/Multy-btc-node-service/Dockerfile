FROM golang:1.9.4

RUN go get github.com/Appscrunch/Multy-back && \
    cd $GOPATH/src/github.com/Appscrunch/Multy-back && \
    git checkout btc-client-nc

RUN go get github.com/Appscrunch/Multy-BTC-node-service && \
    cd $GOPATH/src/github.com/Appscrunch/Multy-BTC-node-service && \
    git pull && \
    make all-with-deps
    #make docker

WORKDIR /go/src/github.com/Appscrunch/Multy-BTC-node-service/cmd

RUN echo "VERSION 02"

ENTRYPOINT $GOPATH/src/github.com/Appscrunch/Multy-BTC-node-service/cmd/client
