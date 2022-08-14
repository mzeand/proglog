# 『Go言語による分散サービス』のコード

書籍: [Go言語による分散サービス](https://www.oreilly.co.jp/books/9784873119977/)

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
