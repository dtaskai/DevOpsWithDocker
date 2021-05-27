FROM node:lts-alpine3.13 AS BUILD_IMAGE

WORKDIR /src/app

COPY ./material-applications/example-frontend/ .

RUN npm install && npm run build

FROM node:lts-alpine3.13

WORKDIR /src/app

COPY --from=BUILD_IMAGE /src/app/build ./build

EXPOSE 5000

ENV REACT_APP_BACKEND_URL=http://localhost:8080/

RUN adduser -D appuser && chmod a+rwx /src/app && npm install -g serve

USER appuser

CMD ["serve","-s","-l","5000","build"]