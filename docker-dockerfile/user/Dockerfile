FROM golang:1.18-alpine
ENV APP_PORT=8080

RUN mkdir /app

RUN addgroup -S fikriksgroup
RUN adduser -S -D -h /app fikriks fikriksgroup
RUN chown -R fikriks:fikriksgroup /app
USER fikriks

COPY main.go /app

EXPOSE ${APP_PORT} 

CMD go run /app/main.go