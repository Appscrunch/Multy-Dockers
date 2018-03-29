FROM golang:1.9.4

RUN go get golang.org/x/net/context
RUN go get google.golang.org/grpc

RUN go get github.com/Appscrunch/Multy-back

RUN cd $GOPATH/src/github.com/Appscrunch/Multy-back && \
    git pull && \
    git checkout btc-client-nc && \
    make all-docker



WORKDIR /go/src/github.com/Appscrunch/Multy-back/cmd

RUN echo "VERSION 02"

ENTRYPOINT $GOPATH/src/github.com/Appscrunch/Multy-back/cmd/multy
