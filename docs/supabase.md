# Supabase

开源后端服务：数据库、登录、存储、实时、自动 API。

- 仓库：https://github.com/supabase/supabase
- 文档：https://supabase.com/docs

## 云端

注册 https://supabase.com 创建项目，控制台可管理表、Auth、Storage。

## 本地 Docker

```bash
git clone --depth 1 https://github.com/supabase/supabase
cd supabase/docker
cp .env.example .env
docker compose up -d
```

按终端与文档中的端口访问 Studio 与 API。  
生产环境请修改默认密钥，并做好备份与网络安全。

## 常见能力

| 模块 | 说明 |
|------|------|
| Database | PostgreSQL |
| Auth | 邮箱 / 社交登录等 |
| Storage | 文件对象存储 |
| Realtime | 订阅数据变更 |
| API | 基于表的自动 REST / 客户端 SDK |
