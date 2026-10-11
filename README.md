# yuzhaohai/html · 静态 HTML 资源仓库

存放供其他项目直接引用的静态 HTML 页面，通过 GitHub Pages / jsDelivr CDN **原样输出**，不会被任何构建流程压缩、改写或套用主题。

## 文件清单

| 文件 | 说明 |
| --- | --- |
| `clock.html` | 时钟 |
| `clock-2.html` | 时钟（变体） |
| `json-tree.html` | JSON 树视图 |
| `shudu.html` | 数独 |
| `sudoku.html` | 数独（变体） |
| `snake.html` | 贪吃蛇 |
| `favicon-96x96.png` | 页面图标（页面内以相对路径引用） |

## 引用方式

推送后即可使用（任选其一）：

**1. jsDelivr CDN —— 无需任何配置，推荐**

```
https://cdn.jsdelivr.net/gh/yuzhaohai/html@main/json-tree.html
```

**2. GitHub Pages —— 需先开启**

仓库 Settings → Pages → Source 选择 `Deploy from a branch` → 分支 `main`，目录 `/ (root)`：

```
https://yuzhaohai.github.io/html/json-tree.html
```

### 使用示例

iframe 嵌入：

```html
<iframe
  src="https://cdn.jsdelivr.net/gh/yuzhaohai/html@main/json-tree.html"
  width="100%"
  height="600"
  frameborder="0"
></iframe>
```

链接引用：

```html
<a href="https://yuzhaohai.github.io/html/json-tree.html">JSON 树视图</a>
```

## 说明

- 根目录的 `.nojekyll` 用于关闭 GitHub Pages 的 Jekyll 处理，保证文件按原样输出、不压缩、不注入主题。
- 新增文件：直接放入根目录，提交推送后即可引用，地址为 `仓库名/文件名`。
- 需要固定版本时，可在 GitHub 上打 tag（如 `v1.0.0`），然后把 jsDelivr 的 `@main` 换成 `@v1.0.0`。
- 这些页面为独立 HTML，可单独打开，不受所属站点构建流程影响。
