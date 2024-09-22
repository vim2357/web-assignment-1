FROM golang:alpine as builder

WORKDIR /app

COPY ./main.go /app/

RUN go build main.go

FROM golang:alpine as runner

WORKDIR /app

COPY --from=builder /app/main /app/

ENTRYPOINT ["/app/main"]
