# 『Go言語による分散サービス』のコード

書籍: [Go言語による分散サービス](https://www.oreilly.co.jp/books/9784873119977/)
[正誤表](https://yoshikishibata.github.io/myhomepage/errata/distributed_services_in_go.html)

# 環境

- golang 1.18
- MaccBook M1
- macOS 12.5

## Chapter 1

### テスト方法

- サーバ起動
```sh

go run ./cmd/server/main.go

```

  - 別のターミナルで実行

```sh

$ ./ch1_local_test.sh
{"offset":0}
{"offset":1}
{"offset":2}


```

## Chapter 2


### Install the protocol compiler plugins

- [gRPC go Quick start](https://grpc.io/docs/languages/go/quickstart/)

```sh
$ go install google.golang.org/protobuf/cmd/protoc-gen-go@v1.28
$ go install google.golang.org/grpc/cmd/protoc-gen-go-grpc@v1.2
$ export PATH="$PATH:$(go env GOPATH)/bin"
```

### Compile

```sh
$ protoc api/v1/*.proto \
  --go_out=. \
  --go_opt=paths=source_relative \
  --proto_path=.
```
