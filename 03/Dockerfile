FROM mirror.gcr.io/golang:1.24-alpine3.22 AS builder

WORKDIR /
COPY main.go .
RUN go build main.go

FROM alpine:3.22

COPY --from=builder /main /

CMD ["./main"]