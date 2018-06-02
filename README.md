### BaiduPCS-Go 百度网盘客户端 WEB UI

这个是 project 只提供 UI 部分， 核心代码在 https://github.com/iikira/BaiduPCS-Go

### 截图

![image](docs/Capture.JPG)

### 前言

本人自用的 UI，只提供简单的链接。可以放在远程服务器里面快速实现离线下载。

### 配置

配置你的登录密码

```
修改index.js里面的
const PASSWORD = 'YourPassword';

使用web时候 需要把`YourPassword`放在密码框里面
```

### 安装

```
npm install
npm run build
npm start
http://localhost:3000
```

### Docker

```
docker build -t baidupcsui .
docker run -d -p 80:3000 -v /downloads:/root/Downloads baidupcsui
```

### 登录 非常重要

在输入框里面输入以下内容，点击 run

```
login -bduss=YOURBUDSS
```

ls
得到目录内所有文件

### 下载

点击文件就可以在后台下载

文件下载完成后会在/downloads 找到， 如果使用docker

如果不使用docker可能会在/用户名/Downloads


### 核心代码更新

在这里下载 最新版本的`linux-amd64.zip`(docker环境下)并解压到根目录

https://github.com/iikira/BaiduPCS-Go/releases

记得运行 chmod u+x ./BaiduPCS-Go (如果不用docker)

