# Ollama

本地运行大语言模型。

- 仓库：https://github.com/ollama/ollama
- 官网：https://ollama.com

## 安装

**Linux：**

```bash
curl -fsSL https://ollama.com/install.sh | sh
```

**macOS / Windows：** 从官网下载安装包。

## 常用命令

```bash
ollama run qwen2.5          # 下载并对话
ollama run deepseek-r1
ollama pull llama3.2
ollama list                 # 已安装模型
ollama rm <模型名>          # 删除
ollama serve                # 仅启动服务（默认 11434）
```

## 对接其他工具

默认 API：`http://127.0.0.1:11434`  
可被 Open WebUI、各类客户端调用。

## 注意

- 模型体积大，注意磁盘与内存
- 显卡可加速，无 GPU 也能 CPU 推理（更慢）
