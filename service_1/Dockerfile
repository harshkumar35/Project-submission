FROM golang:1.22

WORKDIR /app

COPY main.go .

ENV GO111MODULE=off

RUN go build -o server .

EXPOSE 8001

CMD ["./server"]
