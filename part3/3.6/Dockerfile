FROM golang:alpine3.13 AS BUILD_IMAGE

WORKDIR /src/app

COPY ./material-applications/example-backend/ .

RUN go build

FROM scratch

WORKDIR /src/app

ENV REQUEST_ORIGIN=http://localhost:5000

COPY --from=BUILD_IMAGE /src/app/server ./server

EXPOSE 8080

CMD ["./server"]