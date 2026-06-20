# 惜染图库

> 高清随机图片站，动漫美图、AI 绘画、cosplay、手机壁纸，每日更新。

[![Pages](https://img.shields.io/badge/GitHub_Pages-在线预览-pink?logo=github)](https://meshbit.github.io/image-station/)
[![CF Tunnel](https://img.shields.io/badge/Cloudflare_Tunnel-img.okva.cc-orange?logo=cloudflare)](https://img.okva.cc)

## 功能

- **瀑布流首页** — 流式渲染，图到即显，无限滚动加载更多
- **分类搜索** — 实时过滤 30+ 分类（AI 绘画、cosplay、手机壁纸、4K 等）
- **美图广场** — Banner 轮播 + 分类标签切换
- **时间轴归档** — 按月份浏览历史图片
- **随便看看** — 随机打开一张图
- **灯箱预览** — 全屏查看，键盘左右切换，心形点赞
- **暗色模式** — 自动跟随系统 / 手动切换
- **友情链接** — 友链卡片模块
- **移动适配** — 响应式布局，移动端侧栏 + 搜索独立交互
- **PJAX 进度条** — 页面切换顶部渐变色动画
- **登录弹窗** — 遮罩毛玻璃造影效果

## 架构

```
GitHub Pages (docs/)
    ↓
Cloudflare Tunnel (img.okva.cc)
    ↓
Nginx 反向代理 (localhost:8088)
    ↓
api.hefollo.com/AllJsonApi.php?type=分类
```

API 由 [Hefollo 图库](https://hefollo.com) 提供，每次返回随机图片 URL。通过 Nginx 代理解决跨域问题，CF Tunnel 暴露公网。

## 技术栈

| 层 | 技术 |
|---|------|
| 前端 | 原生 HTML + JS + Tailwind CSS CDN |
| 部署 | GitHub Pages (`docs/`) |
| 代理 | Nginx (Docker) + Cloudflare Tunnel |
| API | Hefollo AllJsonApi |

## 本地运行

```bash
# 启动 Nginx 代理 + Tunnel
docker-compose up -d

# 直接访问
http://localhost:8088
```

公网访问：[img.okva.cc](https://img.okva.cc) | [GitHub Pages](https://meshbit.github.io/image-station/)

## 许可证

MIT © 2026
