FROM golang:1.12-alpine
RUN apk update && apk upgrade && \
    apk add --no-cache bash git openssh
WORKDIR /freelancer/rabbitmq-experiments/hello-rabbitmq
COPY go.mod go.sum ./
RUN go mod download
COPY . .
RUN go build -o send .
EXPOSE 8081
CMD ["./send"]