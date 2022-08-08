# 115drive-webdav

[![Release](https://img.shields.io/github/v/release/gaoyb7/115drive-webdav.svg)](https://github.com/gaoyb7/115drive-webdav/releases)
[![Downloads](https://img.shields.io/github/downloads/gaoyb7/115drive-webdav/total)](https://github.com/gaoyb7/115drive-webdav/releases)
[![GitHub Actions](https://github.com/gaoyb7/115drive-webdav/workflows/CI/badge.svg)](https://github.com/gaoyb7/115drive-webdav/actions)
[![Docker Image](https://img.shields.io/docker/pulls/gaoyb7/115drive-webdav.svg?maxAge=2592000)](https://hub.docker.com/r/gaoyb7/115drive-webdav)

115 网盘 WebDav 服务，可配合支持 WebDAV 协议的客户端 App 食用，如 [Infuse](https://firecore.com/infuse)、[nPlayer](https://nplayer.com) 

## 下载
https://github.com/gaoyb7/115drive-webdav/releases

## 运行
需要获取 115 网盘 Cookie 信息，包括 UID、CID、SEID，网页版 Cookie 时效较短，建议抓包 App 请求获取 Cookie，iOS 系统可使用 [Stream](https://apps.apple.com/cn/app/stream/id1312141691) 抓包
```bash
./115drive-webdav --host=0.0.0.0 --port=8080 --user=user --pwd=123456 --uid=xxxxxx --cid=xxxxxxx --seid=xxxxx
```

## Docker 运行
```bash
docker run -d -p 8081:8081 gaoyb7/115drive-webdav \
	--host=0.0.0.0 --port=8081 \
	--user=user --pwd=123456 \
	--uid=xxxxxx \
	--cid=xxxxxx \
	--seid=xxxxxx
```

## 参数说明
```bash
--host
    服务监听地址，默认 0.0.0.0
--port
    服务监听端口，默认 8080
--user
    WebDav 账户用户名，默认 user
--pwd
    WebDav 账户密码，默认 123456
--uid
    115 网盘 Cookie，UID
--cid
    115 网盘 Cookie，CID
--seid
    115 网盘 Cookie，SEID
--config
    从文件中读取配置，参考 config.json.example
```

## 功能支持

- [x] 文件/文件夹查看
- [x] 文件下载
- [x] WebDav 权限校验
- [x] WebDav 在线视频播放
- [ ] 文件上传
- [x] 文件重命名
- [x] 文件删除
- [x] 文件移动
