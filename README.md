# yuzhaohai/html · 静态 HTML 资源仓库

存放供其他项目直接引用的静态 HTML 页面，通过 GitHub Pages **原样输出**，不会被任何构建流程压缩、改写或套用主题。

## 目录结构

| 路径 | 说明 |
| --- | --- |
| `awsome/` | 独立小工具页：时钟、数独、贪吃蛇、JSON 树视图、点名器、家族树等 |
| `fireworks/` | 烟花效果页面 |
| `HTML5_Audio_Visualizer/` | HTML5 音频可视化项目 |
| `favicon-96x96.png` | 页面图标 |

### awsome/ 页面清单

`clock.html`、`clock-2.html`、`json-tree.html`、`shudu.html`、`snake.html`、`sudoku.html`、`FamilyTreeGenerator.html`、`RollCallSystem.html`

## 引用方式（重要）

### HTML 页面：必须用 GitHub Pages

`cdn.jsdelivr.net` 与 `raw.githubusercontent.com` 都会把 `.html` 文件按 `text/plain` 返回（浏览器会显示源码而不是渲染页面），因此 **HTML 页面只能通过 GitHub Pages 引用**。

**开启 Pages（一次性）**：仓库 Settings → Pages → Source 选择 `Deploy from a branch` → 分支 `main`，目录 `/ (root)`。

启用后地址规则：`https://yuzhaohai.github.io/html/<路径>`

| 文件 | 访问链接 |
| --- | --- |
| `awsome/clock.html` | `https://yuzhaohai.github.io/html/awsome/clock.html` |
| `awsome/json-tree.html` | `https://yuzhaohai.github.io/html/awsome/json-tree.html` |
| `fireworks/index.html` | `https://yuzhaohai.github.io/html/fireworks/` |
| `HTML5_Audio_Visualizer/index.html` | `https://yuzhaohai.github.io/html/HTML5_Audio_Visualizer/` |

### jsDelivr：仅用于 JS / CSS / 图片等静态资源（.html 除外）

```
https://cdn.jsdelivr.net/gh/yuzhaohai/html@main/favicon-96x96.png
```

### 使用示例

iframe 嵌入：

```html
<iframe
  src="https://yuzhaohai.github.io/html/awsome/json-tree.html"
  width="100%"
  height="600"
  frameborder="0"
></iframe>
```

链接引用：

```html
<a href="https://yuzhaohai.github.io/html/awsome/clock.html">时钟</a>
```

## 说明

- 根目录的 `.nojekyll` 用于关闭 GitHub Pages 的 Jekyll 处理，保证文件按原样输出、不压缩、不注入主题。
- 新增文件：放入对应目录，提交推送后即可引用，地址为 `仓库名/目录名/文件名`。
- 子目录内的相对资源引用（css / js / mp3 等）会自动拼到同路径下，无需额外处理。
- 需要固定版本时，可在 GitHub 上打 tag（如 `v1.0.0`），jsDelivr 引用中把 `@main` 换成 `@v1.0.0`。
- 这些页面为独立 HTML，可单独打开，不受所属站点构建流程影响。
