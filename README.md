# 技术笔记

Hugo + PaperMod。文章是 `content/posts/` 下的 Markdown。公式在构建时用 KaTeX 渲染，样式打进仓库。推到 `main` 后由 GitHub Actions 发到 GitHub Pages。

## 本机

需要 [Hugo Extended](https://gohugo.io/installation/) ≥ 0.146。克隆时带上主题子模块：

```bash
git clone --recurse-submodules git@github.com:KhazanGu/blog.git
cd blog
hugo server
```

打开 http://localhost:1313/ 。已有仓库补主题：

```bash
git submodule update --init --recursive
```

## 写文章

```bash
hugo new content posts/一篇笔记.md
```

把 `draft = true` 改成 `false`。行内公式用 `\(...\)`，块级用 `$$` 或 `\[...\]`。代码围栏会高亮。

改站点名：编辑 `hugo.toml` 的 `title`。线上：https://khazangu.github.io/blog/ ，细节见 [DEPLOY.md](DEPLOY.md)。
