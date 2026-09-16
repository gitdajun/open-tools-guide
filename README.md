# 开源工具中文指南

本仓库整理常用开源工具的安装与入门用法，方便本地部署与日常使用。

| 工具 | 用途 | 文档 |
|------|------|------|
| [ComfyUI](#1-comfyui) | AI 绘图工作流 | [docs/comfyui.md](docs/comfyui.md) |
| [Ollama](#2-ollama) | 本地大模型运行 | [docs/ollama.md](docs/ollama.md) |
| [Open WebUI](#3-open-webui) | 本地 Chat 界面 | [docs/open-webui.md](docs/open-webui.md) |
| [Excalidraw](#4-excalidraw) | 在线白板 / 流程图 | [docs/excalidraw.md](docs/excalidraw.md) |
| [RustDesk](#5-rustdesk) | 远程桌面 | [docs/rustdesk.md](docs/rustdesk.md) |
| [Godot](#6-godot) | 2D/3D 游戏引擎 | [docs/godot.md](docs/godot.md) |
| [Supabase](#7-supabase) | 后端即服务 | [docs/supabase.md](docs/supabase.md) |

程序请从各项目官方仓库或官网下载；本仓库只提供中文说明与常用命令。

---

## 1. ComfyUI

节点式 AI 绘图工作台，支持文生图、图生图、放大、批量出图等。

**仓库**：https://github.com/comfyanonymous/ComfyUI

### 快速开始（建议有 NVIDIA 显卡）

```bash
git clone https://github.com/comfyanonymous/ComfyUI.git
cd ComfyUI
pip install -r requirements.txt
python main.py
```

浏览器打开终端提示的地址（默认 `http://127.0.0.1:8188`）。  
模型文件放到 `models/checkpoints` 等目录。详见 [docs/comfyui.md](docs/comfyui.md)。

---

## 2. Ollama

在本地运行大模型（DeepSeek、Qwen、Gemma、Llama 等），对话不经过云端 API。

**仓库**：https://github.com/ollama/ollama  
**官网**：https://ollama.com

### 安装与使用

- macOS / Windows：官网下载安装包  
- Linux：

```bash
curl -fsSL https://ollama.com/install.sh | sh
```

```bash
ollama run qwen2.5
ollama run deepseek-r1
ollama list
```

更多见 [docs/ollama.md](docs/ollama.md)。

---

## 3. Open WebUI

本地 Web 聊天界面，可对接 Ollama 等多模型，支持知识库、联网搜索、多用户。

**仓库**：https://github.com/open-webui/open-webui

### Docker 一键（需已安装 Docker，且本机有 Ollama）

```bash
docker run -d -p 3000:8080 \
  --add-host=host.docker.internal:host-gateway \
  -v open-webui:/app/backend/data \
  --name open-webui \
  --restart always \
  ghcr.io/open-webui/open-webui:main
```

浏览器访问 `http://localhost:3000`。详见 [docs/open-webui.md](docs/open-webui.md)。

---

## 4. Excalidraw

手绘风格白板，适合流程图、架构图、原型草图，可自托管。

**仓库**：https://github.com/excalidraw/excalidraw  
**在线**：https://excalidraw.com

本地开发示例：

```bash
git clone https://github.com/excalidraw/excalidraw.git
cd excalidraw
yarn
yarn start
```

详见 [docs/excalidraw.md](docs/excalidraw.md)。

---

## 5. RustDesk

开源远程桌面，支持自建中继服务器，客户端覆盖 Windows / macOS / Linux / Android / iOS。

**仓库**：https://github.com/rustdesk/rustdesk  
**下载**：https://github.com/rustdesk/rustdesk/releases

1. 安装客户端  
2. 需要时可自建 `hbbs` / `hbbr` 中继  
3. 在客户端填写 ID 服务器与密钥  

详见 [docs/rustdesk.md](docs/rustdesk.md)。

---

## 6. Godot

免费开源的 2D / 3D 游戏引擎，MIT 许可，编辑器一体化。

**仓库**：https://github.com/godotengine/godot  
**下载**：https://godotengine.org/download

从官网下载对应系统版本，解压即可运行编辑器，新建 2D/3D 项目开始开发。  
详见 [docs/godot.md](docs/godot.md)。

---

## 7. Supabase

开源 Backend-as-a-Service：Postgres、认证、存储、实时订阅、自动 API。

**仓库**：https://github.com/supabase/supabase  
**文档**：https://supabase.com/docs

本地用 Docker：

```bash
git clone --depth 1 https://github.com/supabase/supabase
cd supabase/docker
cp .env.example .env
docker compose up -d
```

详见 [docs/supabase.md](docs/supabase.md)。

---

## 说明

- 各工具的许可与更新以官方仓库为准  
- 请遵守当地法律与各项目服务条款  
- 本仓库不提供商业支持或付费节点  

## License

MIT License（仅针对本仓库文档与脚本）
