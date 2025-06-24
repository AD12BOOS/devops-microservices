FROM golang:1.21-alpine

WORKDIR /app

COPY . .

RUN apk add --no-cache curl

RUN go build -o app .

CMD ["./app"]
