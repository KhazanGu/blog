+++
date = 2026-09-01T10:00:00+08:00
draft = false
title = "从这里开始写"
tags = ["Hugo", "Markdown"]
categories = ["笔记"]
ShowToc = true
summary = "示例：代码高亮、行内公式和块级公式。删掉这篇，换成你自己的笔记即可。"
+++

这是一篇示例，用来确认主题、代码高亮和 KaTeX 都正常。本地预览：

```bash
hugo server
```

浏览器打开 `http://localhost:1313/`。新文章：

```bash
hugo new content posts/我的标题.md
```

## 代码

下面是一段带高亮的 Go：

```go
package main

import "fmt"

func main() {
	fmt.Println("hello, blog")
}
```

代码围栏会按语言高亮。

## 公式

行内：欧拉公式 \(\mathrm{e}^{i\pi} + 1 = 0\)。

块级（`$$`）：

$$
\int_{-\infty}^{\infty} e^{-x^2}\, dx = \sqrt{\pi}
$$

也可以用 `\[ \]`：

\[
KL(\hat{y} \parallel y) = \sum_{c=1}^{M} \hat{y}_c \log\frac{\hat{y}_c}{y_c}
\]

公式在 **Hugo 构建时** 渲染成 HTML。样式和字体在仓库的 `static/katex/`。

写完推到 `main`，GitHub Actions 会发到 GitHub Pages，步骤见仓库里的 `DEPLOY.md`。
