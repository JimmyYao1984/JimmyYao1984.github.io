# Jimmy Yao's Homepage

本仓库是 GitHub Pages 个人主页,基于 [Chirpy](https://github.com/cotes2020/jekyll-theme-chirpy) 主题(Jekyll),
通过 GitHub Actions 自动构建发布,访问地址:<https://jimmyyao1984.github.io>

## 日常使用(只需记住这两个)

### 1. 写新博客文章

在 `_posts/` 目录新建文件,文件名格式必须是:

```
年-月-日-文章标题.md
例如:2026-11-01-my-first-post.md
```

文件开头写上如下信息(front matter),后面直接写 Markdown 正文:

```markdown
---
title: "文章标题"
date: 2026-11-01 10:00:00 +0800
categories: Life
tags: [笔记, 随笔]
---

正文从这里开始……
```

### 2. 添加独立页面(如 Projects、友链等)

在 `_tabs/` 目录新建 `.md` 文件,例如 `_tabs/projects.md`:

```markdown
---
icon: fas fa-folder-open   # 侧边栏图标(FontAwesome)
order: 5                    # 菜单排序
---

页面内容(Markdown)……
```

保存后 push 到 GitHub,Actions 会自动构建,约 1–2 分钟后线上生效。

## 目录结构速查

| 目录/文件 | 作用 |
|---|---|
| `_posts/` | 博客文章 |
| `_tabs/` | 顶部导航的独立页面(About、Archives、Categories、Tags…) |
| `_config.yml` | 站点核心配置:标题、头像、社交链接、评论、主题色等 |
| `assets/img/` | 图片(头像、文章配图)放这里 |
| `.github/workflows/pages-deploy.yml` | 自动构建部署脚本(不用改) |

## 常用个性化配置(`_config.yml`)

- `avatar: /assets/img/avatar.png` — 侧边栏头像(把图片放到 `assets/img/`)
- `theme_mode: # light | dark` — 留空则跟随系统,并可在左下角切换深色/浅色
- `social:` — 邮箱、GitHub、Twitter 等社交链接
- `comments.provider:` — 评论系统,可选 `giscus`(基于 GitHub Discussions,推荐)/ `disqus` / `utterances`
- `analytics:` — 接入 Google Analytics 等统计

## 首次部署设置(只需做一次)

1. 推送到 GitHub 后,进入仓库 **Settings → Pages**,把 **Source** 设为 **GitHub Actions**。
2. 到仓库 **Actions** 标签页确认 `Build and Deploy` 工作流成功运行。
3. 打开 <https://jimmyyao1984.github.io> 查看效果。

## 本地预览(可选)

```bash
bundle install
bundle exec jekyll serve
# 打开 http://127.0.0.1:4000
```
