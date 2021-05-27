FROM golang:alpine3.13

WORKDIR /src/app

COPY ./material-applications/example-backend/ .

EXPOSE 8080

ENV REQUEST_ORIGIN=http://localhost:5000

RUN adduser -D appuser && chmod a+rwx /src/app && go build

USER appuser

CMD ["./server"]