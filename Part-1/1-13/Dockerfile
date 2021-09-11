FROM golang:1.16

ENV REQUEST_ORIGIN=http://localhost:5000

EXPOSE 8080

COPY . ./myapp
WORKDIR ./myapp

RUN go build

CMD ["./server"]




