FROM golang:1.22.4-alpine

WORKDIR /app

COPY go.mod ./
RUN go mod download || true

COPY . .

RUN go build -o app .

CMD ["./app"]
