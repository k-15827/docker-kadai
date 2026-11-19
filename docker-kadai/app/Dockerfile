FROM golang:1.22

# 作業ディレクトリの指定
WORKDIR /app

# MySQLドライバのダウンロード
COPY go.mod ./

RUN go mod download

COPY . .

RUN go mod tidy

RUN go build -o ./main .

CMD ["./main"]
