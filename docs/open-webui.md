# Open WebUI

本地 Web 聊天前端，常与 Ollama 搭配。

- 仓库：https://github.com/open-webui/open-webui

## Docker 部署

需已安装 Docker，且本机 Ollama 在运行：

```bash
docker run -d -p 3000:8080 \
  --add-host=host.docker.internal:host-gateway \
  -v open-webui:/app/backend/data \
  --name open-webui \
  --restart always \
  ghcr.io/open-webui/open-webui:main
```

访问：`http://localhost:3000`

首次进入会创建管理员账号。在设置中确认 Ollama 连接地址（Docker 下多为 `http://host.docker.internal:11434`）。

## 能力概览

- 多模型切换
- 知识库 / 文档问答
- 联网搜索（需配置）
- 多用户与权限

## 更新

```bash
docker pull ghcr.io/open-webui/open-webui:main
docker rm -f open-webui
# 再执行上面的 run 命令（数据在 volume 中会保留）
```
