FROM golang:latest

WORKDIR /server
COPY go.mod ./
COPY go.sum ./

RUN go mod download

COPY . ./

EXPOSE 8001

RUN go build server.go

CMD [ "./server" ]
