# 🎨 惜染图库 — 随机图片站

基于 [hefollo.com](https://hefollo.com/) API 的随机图片浏览站，nginx + 纯前端。

## 快速启动

```bash
docker compose up -d
```

访问 `http://localhost:8088`

## 功能

- **42 个分类** 随机图片
- 分类过滤 / 随机换一批 / 加载更多
- Lightbox 大图浏览 + 键盘导航
- 视频自动播放
- 暗色主题，响应式布局

## 技术栈

- nginx:alpine 反向代理 hefollo API（解决跨域）
- 纯 HTML/CSS/JS，零依赖

## 项目结构

```
site/index.html      — 前端页面
nginx/default.conf   — nginx 配置（含 API 反向代理）
docker-compose.yml   — Docker 编排
```
