FROM golang:alpine AS builder

WORKDIR /src

COPY . .

RUN go build -ldflags '-s -w' print.go

FROM scratch

WORKDIR /

COPY --from=builder /src / 

CMD ["./print"]