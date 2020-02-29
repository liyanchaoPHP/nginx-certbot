# A repository fork from [https://github.com/wmnnd/nginx-certbot](@wmnnd)

## 用途

使用`docker-compose`配置nginx并申请certbot证书。

## 文件说明

* `init-letsencrypt.sh`：获取Let's Encrypt证书；
* `data/nginx`：nginx配置文件目录；
* `docker-compose.yml`：服务配置；

## 使用说明

1.解析域名到你的服务器；

2.安装docker-compose，参考： <a href="https://www.4spaces.org/centos-install-docker-compose/" target="_blank">CENTOS安装Docker Compose</a>；

3.修改配置；

* 修改`init-letsencrypt.sh`文件中的域名及邮箱；
* 修改`data/nginx`中的域名；

4.申请证书

```
chomod +x ./init-letsencrypt.sh

sudo ./init-letsencrypt.sh
```

5.启动服务

```
 docker-compose up -d
```

## 测试环境

* CentOS Linux release 7.3.1611 (Core)  <a href="https://www.4spaces.org/best-details-to-buy-banwagonhost/" target="_blank">搬瓦工</a>