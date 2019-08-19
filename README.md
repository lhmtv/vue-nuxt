# ssr-nuxt

> vue服务端渲染pm2监控

## Build Setup

``` bash
# 准备工作

1. npm install

2.修改package.json文件
"scripts": {
    "dev": "nuxt",
    "build": "nuxt build",
    "start": "PORT=3000 nuxt start",
    "generate": "nuxt generate"
  },
3. npm run build

4. 把生成的.nuxt static nuxt.config.js package.json放到服务器上

# Centos配置

1. 安装node.js并配置全局变量

2. 安装nginx并配置
upstream nuxtserver {
  server 127.0.0.1:3000;
  keepalive 64;
}
server {
  listen     80;
  server_name localhost;
  location /{
    proxy_pass http://nuxtserver
  }
}

3. 安装pm2

4. 进入项目目录执行命令pm2 start npm -- start
--如果不用pm2直接命令npm start就可以了


