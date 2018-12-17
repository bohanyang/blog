---
title: "在墙内流畅使用 Docker 的奇技淫巧"
date: 2018-07-22T21:58:00+08:00
draft: false
categories: ["experience"]
tags: ["docker", "gfw"]
keywords: ["Docker", "被墙"]
---

## 使用官方一键脚本安装

使用 DaoCloud 的镜像下载脚本：
{{< highlight sh >}}
curl -fsSL https://get.daocloud.io/docker -o get-docker.sh && chmod +x get-docker.sh
{{< / highlight >}}
指定仓库镜像并运行脚本：

~~使用阿里云镜像：~~ 这个貌似炸掉了……
{{< highlight sh >}}
./get-docker.sh --mirror "Aliyun"
{{< / highlight >}}
使用微软 Azure 镜像：
{{< highlight sh >}}
./get-docker.sh --mirror "AzureChinaCloud"
{{< / highlight >}}
<!--more-->
使用 DaoCloud 镜像：
{{< highlight sh >}}
DOWNLOAD_URL="https://download.daocloud.io/docker" ./get-docker.sh
{{< / highlight >}}
使用清华 TUNA（北京教育网）镜像：
{{< highlight sh >}}
DOWNLOAD_URL="https://mirrors.tuna.tsinghua.edu.cn/docker-ce" ./get-docker.sh
{{< / highlight >}}
使用中科大（合肥三线）镜像：
{{< highlight sh >}}
DOWNLOAD_URL="https://mirrors.ustc.edu.cn/docker-ce" ./get-docker.sh
{{< / highlight >}}
## 配置 Docker Hub 镜像

### 方法一：[DaoCloud 加速器](https://www.daocloud.io/mirror)

### 方法二：[微软 Azure Docker Hub 镜像](https://mirror.azure.cn/help/docker-registry-proxy-cache.html)
