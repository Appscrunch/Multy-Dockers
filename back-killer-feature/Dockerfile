FROM golang:1.9.4

RUN go get -u github.com/vadimicus/Multy-KillerBack


WORKDIR $GOPATH/src/github.com/vadimicus/Multy-KillerBack

#RUN go build $GOPATH/src/github.com/vadimicus/Multy-KillerBack/main.go

RUN echo "VERSION 02"

ENTRYPOINT go run $GOPATH/src/github.com/vadimicus/Multy-KillerBack/main.go
#CMD["go run", "$GOPATH/bit/github.com/vadimicus/Multy-KillerBack/main.go"]
