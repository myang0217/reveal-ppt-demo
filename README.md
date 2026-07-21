# reveal.js 幻灯片示例

一份用 [reveal.js](https://revealjs.com) 做的幻灯片,内容就是「reveal.js 是怎么回事」。

**在线观看:** https://myang0217.github.io/reveal-ppt-demo/

## 这是什么

幻灯片不是 `.pptx`,而是一个 `index.html`。每一页幻灯片就是页面里的一个 `<section>` 标签:

```html
<div class="slides">
  <section><h2>第一页</h2></section>
  <section><h2>第二页</h2></section>
</div>
```

reveal.js 本体和插件全部从 CDN 加载,所以这个仓库只有 `index.html` 一个文件,不需要 `npm install`,也不需要构建。

## 用法

- **在线看**:点上面的链接。
- **本地看**:把 `index.html` 用浏览器打开即可(需要联网加载 CDN)。
- **改内容**:编辑 `index.html`,复制一个 `<section>` 块改里面的文字,提交后 GitHub Pages 约 1 分钟自动更新。
- **换主题**:改 `<head>` 里 `theme/white.css` 这一行,可选 `black` `league` `serif` `moon` `solarized` `dracula` 等。
- **导出 PDF**:网址后加 `?print-pdf`,再用浏览器打印 → 另存为 PDF。

## 快捷键

| 键 | 作用 |
|---|---|
| `空格` / `方向键` | 翻页(左右换章节,上下走同章节的子页) |
| `Esc` / `O` | 鸟瞰全部幻灯片的网格视图 |
| `S` | 演讲者视图(备注 + 计时 + 下一页预览) |
| `F` / `B` | 全屏 / 黑屏 |
| `Alt` + 点击 | 局部放大 |
| `?` | 列出所有快捷键 |

## 演示里用到的特性

- 二维导航:`<section>` 嵌套 `<section>` 做纵向下钻
- 渐进显示:`class="fragment"`
- 代码高亮与分步聚焦:`data-line-numbers="|2-4|6-7"`
- LaTeX 公式:`$...$` / `$$...$$`,由 KaTeX 插件渲染
- 整页背景:`data-background-color` / `-image` / `-video` / `-iframe`
- 演讲者备注:`<aside class="notes">`
