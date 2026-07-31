# 文件库页面视图切换原型

文件库管理页面的 HTML 交互原型项目，包含视图切换（卡片/列表）、排序、分页等交互演示，以及若干用于跳转测试的页面。

## 目录结构

```
-/
├── index.html          # 首页：文件库视图切换 Mockup
├── page1.html          # 跳转测试页 1：数据表格
├── page2.html          # 跳转测试页 2：卡片列表
├── page3.html          # 跳转测试页 3：表单交互
├── vercel.json         # Vercel 静态部署配置
├── docs/               # 需求文档
│   └── 需求说明.md      # 文件库页面需求说明
└── README.md           # 项目说明
```

## 页面说明

| 页面 | 说明 |
|------|------|
| `index.html` | 文件库视图切换 Mockup，支持卡片/列表视图切换、排序、分页 |
| `page1.html` | 数据表格：设备运行状态列表 |
| `page2.html` | 卡片列表：文档卡片展示 |
| `page3.html` | 表单交互：表单提交本地提示 |

所有页面均为纯静态、无外部依赖，互相通过相对路径跳转。

## 需求文档

见 [`docs/需求说明.md`](docs/需求说明.md)。

## 本地运行

无需构建，直接双击 `index.html` 即可在浏览器打开；或启动任意静态服务器：

```bash
python -m http.server 8080
```

## 部署到 Vercel

1. 将本仓库导入 Vercel（通过 GitHub 或 `vercel` CLI）。
2. 项目设置中 **Root Directory 保持默认（仓库根目录）**，Framework Preset 选择 `Other`（纯静态）。
3. 无需构建命令，部署后 `index.html` 即为站点首页。

> 说明：`vercel.json` 中的 `cleanUrls` 已开启，访问时无需带 `.html` 后缀（如 `/page1`）。
