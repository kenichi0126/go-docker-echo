FROM golang:1.14

ENV GO111MODULE=on

WORKDIR /go/src/github.com/kenichi0126/go-docker-echo

COPY go.mod go.sum ./
RUN go mod download

COPY . .
RUN go build .

RUN go get github.com/pilu/fresh

EXPOSE 8080

CMD ["fresh"]
