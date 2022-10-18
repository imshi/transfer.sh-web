# transfer.sh-web
- 该仓库为 [transfer.sh](https://github.com/dutchcoders/transfer.sh/) 项目的前端样式文件
- [2020.01.07] fork 自 [transfer.sh-web](https://github.com/dutchcoders/transfer.sh-web) ，改动如下：
    - 精简部分内容：去除图片、推广、多余的example
    - 根据国人使用习惯重新排版，参考图：![transfer.sh-web](http://cdn.imwang.top/article/transfer.jpg)

## How to use it

You must specify `web-path` directory, pointing to `dist` generated folder (Grunt & bindata)

Sample :
```
docker run -d -v /folder:/uploads -v /folder/dist:/webapp --publish 5000:8080 dutchcoders/transfer.sh:latest --provider local --basedir /uploads --web-path /webapp/
```
## Requirement
You must install first :
* Grunt
* Bower
* Go & go-bindata (go get -u github.com/shuLhan/go-bindata/...)

## Initialization

NPM
```
npm install
```

Bower

*Please*, specify to Bower where to install its packets via .bowerrc, to the `src/bower_components` directory
```
bower install
```

## Build
```
$ grunt build
$ go generate .
```

## Verify
You should see a `dist` directory, where all the basic .html are generated.
