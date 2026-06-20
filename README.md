# 🎨 惜染图库 — 42 个分类随机高清图片站

基于 [hefollo.com](https://hefollo.com/) API，42 个分类随机浏览：**4K 壁纸、AI 绘画、动漫、COS、手机壁纸、表情包**……

🌐 **在线地址：** [meshbit.github.io/image-station](https://meshbit.github.io/image-station/)

## 快速启动

```bash
docker compose up -d
```

本地访问 `http://localhost:8088`

## 功能

- 🏷️ **42 个分类** — 4K 壁纸、AI 绘画、动漫、COS、美女、手机壁纸、表情包……
- 🎲 随机换一批 / 加载更多
- 🔍 Lightbox 大图浏览 + 键盘 ← → 切换
- 🎬 视频自动播放
- 🌙 暗色主题，手机端适配
- ☁️ 自动切换 API 地址（本地 nginx 代理 / 公网 `img.okva.cc`）

## 技术栈

- **前端：** 纯 HTML/CSS/JS（零框架依赖），GitHub Pages 托管
- **后端代理：** nginx:alpine Docker，反向代理 hefollo API
- **公网通道：** Cloudflare Tunnel (`img.okva.cc`)

## 项目结构

```
site/index.html      — 前端页面
docs/index.html      — GitHub Pages 副本
nginx/default.conf   — nginx 配置（API 反向代理）
docker-compose.yml   — Docker 编排
```

## 仓库

🔗 [github.com/meshbit/image-station](https://github.com/meshbit/image-station)
