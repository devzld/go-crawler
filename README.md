# go-crawler
A distributed crawler based on Golang.

---

Details:

[https://blog.csdn.net/chao2016/article/details/81697353](https://blog.csdn.net/chao2016/article/details/81697353)


Tree:

```
go-crawler
├── README.md
├── engine
│   ├── concurrent.go (update)
│   ├── simple.go (update)
│   └── types.go
├── fetcher
│   └── fetcher.go (update)
├── main.go (update)
├── model
│   └── profile.go
├── scheduler
│   └── simple.go (update)
└── zhenai
    └── parser
        ├── city.go
        ├── citylist.go
        ├── citylist_test.go
        ├── citylist_test_data.html
        ├── profile.go
        ├── profile_test.go
        └── profile_test_data.html
```

Download:

```
git clone git@github.com:chao2015/go-crawler.git
```

or download the previous version via [the release page](https://github.com/chao2015/go-crawler/releases)

dependences:

```
// 1. docker 18.06.0-ce
// 2. 安装elasticsearch
docker run -d -p 9200:9200 elasticsearch
// 3. 安装elastic client:
go get -v gopkg.in/olivere/elastic.v5
```


Run:

```
docker ps

// 若有(elasticsearch CONTAINER ID)
docker kill 6a8ea105cbc6

docker run -d -p 9200:9200 elasticsearch

mv go-crawler/ $GOPATH/src/
cd $GOPATH/src/go-crawler/
go run main.go
go run frontend/starter.go
// http://localhost:8888
// 搜索示例：男 已购房 已购车 Age:(<30) Height:(>180)
```
Have fun! ^_^
