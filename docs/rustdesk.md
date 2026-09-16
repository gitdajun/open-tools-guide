# RustDesk

开源远程桌面软件。

- 仓库：https://github.com/rustdesk/rustdesk
- 发布页：https://github.com/rustdesk/rustdesk/releases

## 客户端

从 Releases 下载对应平台安装包（Windows / macOS / Linux / Android 等）。

## 自建服务器（可选）

默认可走公共服务器；对隐私或稳定性有要求时可自建：

- `hbbs`：ID / 信号服务
- `hbbr`：中继服务

官方提供 Docker 与二进制部署说明。部署后在客户端「网络」中填写 ID 服务器、中继服务器与 Key。

## 使用要点

1. 双方安装客户端
2. 被控端记下 ID 与临时密码（或设置永久密码）
3. 主控端输入 ID 连接

注意防火墙放行相关端口（自建时按文档开放）。
