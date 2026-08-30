# Sikang 的个人网站

基于 [Hugo](https://gohugo.io/) 静态站点生成器和 [HugoBlox Academic](https://github.com/HugoBlox/hugo-theme-academic-cv) 学术主题搭建的个人主页，部署于 GitHub Pages：

👉 https://gskgskgsk.github.io/sikangLab/

## 技术栈

| 部分 | 技术 |
| ---- | ---- |
| 站点生成 | Hugo 0.165（extended） |
| 主题 | HugoBlox Academic（kit，Tailwind CSS v4） |
| 搜索 | Pagefind |
| 部署 | GitHub Pages + GitHub Actions（push 自动构建发布） |

## 目录结构

```
├── .github/workflows/gh-pages.yml   # 自动部署流水线
├── config/_default/                 # 站点配置
│   ├── hugo.yaml                    #   Hugo 基础配置（语言/baseURL）
│   ├── languages.yaml               #   语言（简体中文）
│   ├── menus.yaml                   #   顶部导航菜单
│   ├── module.yaml                  #   Hugo 模块（主题）
│   └── params.yaml                  #   站点品牌、配色、功能开关
├── content/                         # 网站内容（Markdown）
│   ├── _index.md                    #   首页（区块组合）
│   ├── experience.md                #   经历/技能/奖项/语言 页
│   ├── links.md                     #   友链页
│   ├── blog/                        #   博客文章
│   ├── projects/                    #   项目作品
│   └── publications/                #   论文（可按需添加）
├── data/authors/me.yaml             # ⭐ 你的个人信息（名字/简介/经历/技能）
└── assets/media/authors/me.png      # ⭐ 你的头像（替换为真实照片）
```

## 本地开发

```bash
# 1. 安装依赖（Hugo 0.165+、Go、pnpm 一次性装好）
pnpm install

# 2. 本地实时预览（默认 http://localhost:1313）
hugo server --disableFastRender
```

## 日常更新

### 写一篇新博客

在 `content/blog/` 下新建文件夹，例如 `content/blog/my-first-post/index.md`：

```markdown
---
title: '文章标题'
summary: 文章摘要
date: 2026-08-18
authors:
  - me
tags:
  - 标签1
---

正文内容……
```

### 修改个人信息

编辑 `data/authors/me.yaml`（姓名、简介、链接、教育/工作经历、技能、语言、奖项）。

### 新增项目 / 论文

- 项目：在 `content/projects/<名称>/index.md` 新建（可选放 `featured.png` 封面图）
- 论文：在 `content/publications/<名称>/` 新建 `index.md` 和 `cite.bib`

### 更新后发布

```bash
git add .
git commit -m "更新内容"
git push origin main
```

push 后 GitHub Actions 会自动构建并部署，约 1–2 分钟后访问站点即可看到更新。

## 需要你替换的内容（占位符）

- `data/authors/me.yaml`：教育经历、工作经历、奖项等示例内容
- `assets/media/authors/me.png`：示例渐变头像
- `content/projects/example-project/`：示例项目
- `config/_default/params.yaml` 中 `identity.name` 等品牌信息

## 许可证

站点源码基于 [HugoBlox](https://github.com/HugoBlox/kit) 模板（MIT License）搭建。
