FROM golang

#WORKDIR /app
WORKDIR /go/src/app
ADD . .
RUN go mod init
RUN go build -o /meugo
ENTRYPOINT /meugo
