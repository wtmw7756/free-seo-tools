# 在 DatabaseMart VPS 上轻松安装 Coolify（Ubuntu 24.04 LTS 版）

Coolify 是一个现代化的开源自托管平台，可作为 Heroku 等服务的替代方案。本指南将详细介绍如何在 DatabaseMart 的 Ubuntu 24.04 LTS VPS 上安装 Coolify。

## 系统要求

开始安装前，请确保您的 VPS 满足以下最低配置：

- 运行 Ubuntu 24.04 LTS 操作系统
- 2 核 CPU
- 2 GB 内存（建议 4 GB 以获得更好性能）
- 开放 22 端口用于 SSH 访问

## 准备工作

1. 已注册的域名
2. 基础的 Linux 命令行知识

👉 [【点击查看】2025年最新 DatabaseMart 优惠码及特价云服务器方案汇总](https://bit.ly/DatabaseMart)

## 安装步骤详解

### 第一步：获取 VPS 服务器

在 DatabaseMart 上选择 Ubuntu 24.04 LTS 操作系统的 Linux VPS 服务器。

### 第二步：初始服务器设置

通过 SSH 连接到您的 VPS：

bash
ssh root@your_server_ip

更新系统软件包：

bash
sudo apt update && sudo apt upgrade -y

### 第三步：安装 Coolify

运行安装脚本（快速安装方法）：

bash
curl -fsSL https://cdn.coollabs.io/coolify/install.sh | bash

安装过程可能需要几分钟时间。

### 第四步：访问 Coolify

安装完成后，通过以下地址访问 Coolify：

http://yourIP:8000

然后创建管理员账户。

### 第五步：初始配置

完成以下设置：

1. 选择部署方式：建议选择"远程服务器"
2. SSH 密钥设置：
   - 如果已有 SSH 私钥，选择"是"
   - 如果没有，选择"否（为我创建一个）"

编辑 `~/.ssh/authorized_keys` 文件添加公钥。

### 第六步：设置完整域名

建议不要直接使用 IP 地址访问 Coolify，而是设置完整的域名并启用 SSL：

1. 在域名注册商处添加 A 记录，指向服务器 IP
2. 等待 DNS 解析生效
3. 在 Coolify 仪表板的"设置"中配置实例域名（务必包含 `https://`）

## 后续操作

成功安装 Coolify 后，您可以通过仪表板：

- 部署各种应用程序
- 管理数据库
- 配置服务

Coolify 支持通过 Git、Docker 等多种方式部署应用。

## 安全建议

为了增强安全性，您可以：

- 设置双重认证(2FA)
- 禁用未使用的 IPv6 功能

现在，您已经可以安全地使用 Coolify 来管理您的应用和服务了！