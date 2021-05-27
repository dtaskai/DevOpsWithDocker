FROM golang:alpine3.13 AS BUILD_IMAGE

WORKDIR /src/app

COPY ./material-applications/example-backend/ .

RUN go build

USER appuser

FROM golang:alpine3.13

WORKDIR /src/app

ENV REQUEST_ORIGIN=http://localhost:5000

RUN chmod a+rwx /src/app && adduser -D appuser

COPY --from=BUILD_IMAGE /src/app/server /src/app/

EXPOSE 8080

CMD ["./server"]