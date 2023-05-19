FROM golang:1.16
WORKDIR /go/src/github.com/PicPay/picpay-jr-devops-challenge/services/go
ADD . .

RUN go env -w GO111MODULE=auto
RUN go mod init
RUN go mod tidy

EXPOSE 8082

ENTRYPOINT [ "go" , "run",  "main.go" ]