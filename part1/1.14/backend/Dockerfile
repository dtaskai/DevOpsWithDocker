FROM golang:alpine3.13

WORKDIR /src/app

COPY ./material-applications/example-backend/ .

EXPOSE 8080

ENV REQUEST_ORIGIN=http://localhost:5000

RUN go build

CMD ["./server"]