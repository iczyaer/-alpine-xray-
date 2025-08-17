# Alpine Xray 一键安装脚本

这是一个为 **Alpine Linux** 系统设计的 Xray 一键安装脚本，用于快速部署最新版本的 Xray 代理服务。脚本支持交互式配置，生成标准 VMess 链接，并自动配置开机启动，适合快速搭建代理服务器。

仓库地址: [https://github.com/iczyaer/alpine-xray](https://github.com/iczyaer/alpine-xray)
## 功能特性

- **自动安装最新 Xray**：从 GitHub 获取并安装最新版本的 Xray。
- **交互式配置**：
  - 端口：默认 42003，可自定义。
  - WebSocket 路径：必须输入，无默认值。
  - Host 域名：必须输入，无默认值。
  - 自动生成随机 UUID 作为客户端 ID。
- **生成 VMess 链接**：安装完成后输出标准 VMess URL，方便导入客户端。
- **开机自启**：使用 OpenRC 配置 Xray 服务，确保系统重启后自动运行。
- **Alpine Linux 优化**：专为 Alpine Linux 设计，依赖最小化。

## 依赖要求

- **操作系统**：Alpine Linux
- **权限**：需要 root 权限运行脚本
- **网络**：服务器需能访问 GitHub（下载 Xray）和外部网络
- **软件包**：脚本会自动安装以下依赖：
  - `curl`
  - `unzip`
  - `jq`
  - `openrc`
 
## 安装方法
克隆仓库或下载脚本：
   ```bash
   git clone https://github.com/iczyaer/alpine-xray.git
   cd alpine-xray
   ```

或者直接下载：
   
