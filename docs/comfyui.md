# ComfyUI

节点式 AI 图像工作流工具。

- 仓库：https://github.com/comfyanonymous/ComfyUI
- 默认端口：8188

## 环境建议

- Python 3.10+、Git
- NVIDIA 显卡 + 较新驱动（CPU 可跑但很慢）
- 可选：使用官方或社区整合包简化依赖

## 安装示例

```bash
git clone https://github.com/comfyanonymous/ComfyUI.git
cd ComfyUI
pip install -r requirements.txt
python main.py
```

访问：`http://127.0.0.1:8188`

## 常用目录

| 路径 | 用途 |
|------|------|
| `models/checkpoints` | 大模型 |
| `models/vae` | VAE |
| `models/loras` | LoRA |
| `models/controlnet` | ControlNet |
| `input` / `output` | 输入输出图 |

## 入门提示

1. 先加载一个基础 checkpoint 工作流
2. 队列一次生成，确认显存与路径无误
3. 再逐步加放大、重绘、批量节点

工作流可导出为 JSON，便于分享与复用。
