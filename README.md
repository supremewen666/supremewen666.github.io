# sprw.github.io

白底、石墨灰文字、少量紫色链接的个人主页。使用系统无衬线字体，12–13px 正文、14px 分区标题与细分隔线组织内容，减少页眉和段落留白。

## 结构

- 简介：以电脑端为主，个人信息、教育、实习、项目、论文、兴趣从上到下单列排列。
- 个人感想：文字列表、分类筛选、展开阅读。
- 顶部仅保留“简介 / 个人感想”，右上角切换中英文。

页面没有框架、外部字体或运行依赖。支持手机、键盘切换、语言偏好保存及减少动画偏好。

## 修改

编辑 `index.html`。中文在 `.zh` 元素内，英文在 `.en` 元素内。资料和文章中尚未填写的内容均为占位，发布个人内容时请替换为真实信息。

新增博客条目可复制 `.post-card`，分类用 `data-category="learning"` 或 `data-category="life"`。配色与字体在 CSS 开头定义。

## 预览与部署

```sh
python3 -m http.server 8000
```

文件可直接打开。`#about` 与 `#blog` 对应两个视图。

推送到 `main` 自动触发 GitHub Pages 工作流。Settings → Pages 的 Source 为 GitHub Actions。

主页：https://supremewen666.github.io/

仓库：https://github.com/supremewen666/supremewen666.github.io

本轮排版参考：https://paco.me/ 、https://antfu.me/ 、https://overreacted.io/ 。未复制参考网站的文案和个人资料。
