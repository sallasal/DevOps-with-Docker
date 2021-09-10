FROM golang:1.16

EXPOSE 8080

COPY . ./myapp
WORKDIR ./myapp

RUN go build

CMD ["./server"]




