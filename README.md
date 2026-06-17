# Ulink IB · 校园 3D 导览 / Campus 3D Guide

领科教育 IB 学部新生校园导览。纯静态站点,无后端、无构建步骤。

## 页面

| 文件 | 说明 |
|---|---|
| `index.html` | 欢迎封面(全屏校园实拍照 + 珊瑚橙 "Let's go" 按钮) |
| `campus.html` | 交互式 3D 校园地图(Three.js):拖拽旋转、滚轮缩放、点击建筑看双语信息;顶部可切到「IB 学部」一层平面 |
| `logo.png` | 校徽 |
| `assets/campus.png` | 封面背景照 |

「Let's go」从封面跳到 `campus.html`。

## 本地预览

ES Module + importmap 需要通过 HTTP 打开(不能直接双击):

```bash
python3 -m http.server 8123
# 然后浏览器打开 http://localhost:8123/
```

## 部署(GitHub Pages)

仓库根目录直接作为站点根。推送后,在仓库 **Settings → Pages → Build and deployment → Source: Deploy from a branch → main / (root)** 即可。
访问地址形如 `https://<用户名>.github.io/<仓库名>/`。

> 注:liquid glass 折射效果在 Chrome / Edge 内核完整生效,Safari 会自动降级为普通毛玻璃。
