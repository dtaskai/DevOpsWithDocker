FROM golang:alpine3.13

WORKDIR /src/app

COPY ./material-applications/example-backend/ .

EXPOSE 8080

ENV REQUEST_ORIGIN=http://localhost:5000

RUN adduser -D appuser

RUN chmod a+rwx /src/app

USER appuser

RUN go build

CMD ["./server"]