FROM golang AS buildando

#WORKDIR /app
WORKDIR /go/src/app
ADD . .
RUN go mod init
RUN go build -o meugo

FROM alpine
WORKDIR /app
COPY --from=buildando /go/src/app/meugo /app
ENTRYPOINT ./meugo
