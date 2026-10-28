# sprw.github.io

一个轻量的双语个人主页。白底、细边框、紧凑简介，个人感想使用独立的博客视图。

- 简介：左侧个人资料，右侧双列教育、实习、项目、论文和兴趣信息框。
- 个人感想：风景横幅、文章卡片、分类筛选、展开阅读。
- 顶部仅有“简介 / 个人感想”，右上角中英文切换，支持语言偏好保存。
- 无框架、无外部运行依赖；支持手机、键盘操作、减少动画偏好及 A4 打印。

## 编辑内容

直接编辑 `index.html`。每段中文放在 `.zh` 元素中，英文放在 `.en` 元素中，无需另外维护翻译字典。

个人经历、邮箱、照片与论文尚为占位，替换时请填写真实资料。博客中两篇条目标记为“模板 · 待发布”，不要将其视作本人已发表文章。新增文章可复制 `.post-card`，设置 `data-category="learning"` 或 `data-category="life"`，并修改中英文标题、摘要和正文。

照片可以将 `.portrait` 占位替换为 `<img>`，使用本地 `./assets/` 路径。新增资源时，请同步修改 `.github/workflows/pages.yml` 的复制步骤；现有工作流仅复制 `assets/favicon.svg`。

配色与字号位于 CSS 开头；中文使用系统宋体/楷体，英文使用 Times New Roman，有系统衬线回退。

## 预览与发布

```sh
python3 -m http.server 8000
```

打开 http://localhost:8000 。文件也可直接打开；`#about` 和 `#blog` 分别对应两个视图。

代码仓库：https://github.com/supremewen666/supremewen666.github.io

主页：https://supremewen666.github.io/

推送到 `main` 后，GitHub Actions 自动部署。仓库 Settings → Pages 的 Source 应为 GitHub Actions。

视觉结构参考用户指定的博客：封面、波浪分界与文章卡片；本站使用原创 SVG 图形和自己的占位内容，未复制参考站的文章和图片。
