FROM golang:1.18-alpine
ENV APP_PORT=8080

ARG app=main

RUN mkdir app
COPY main.go app
RUN mv app/main.go app/${app}.go

EXPOSE ${APP_PORT} 

ENV app=${app}
CMD go run app/${app}.go