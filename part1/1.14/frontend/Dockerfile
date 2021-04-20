FROM node:lts-alpine3.13

WORKDIR /src/app

COPY ./material-applications/example-frontend/ .

EXPOSE 5000

ENV REACT_APP_BACKEND_URL=http://localhost:8080/

RUN npm install && npm run build && npm install -g serve 

CMD ["serve","-s","-l","5000","build"]