# sprw.github.io

白色背景、自然分节、少量棕色链接与简洁文字排版的中英文个人主页。纯静态网站，无需安装依赖，可直接打开 `index.html`。

## 页面结构

个人联系方式 → 教育经历 → 实习经历 → 项目经历 → 论文发表 → 兴趣方向 → 个人感想。

支持顶部文字目录、章节跳转与高亮、移动端自动换行目录、右上角中英文切换、语言偏好保存、返回顶部、键盘导航和减少动画偏好。

## 修改内容

- 中文：编辑 `index.html` 中的正文。
- 英文：编辑 `index.html` 底部的 `en` 字典，键与 `data-i18n` 对应。
- 邮箱：将占位内容替换为真实邮箱，并把外层 `<div class="contact">` 改为 `<a class="contact" href="mailto:你的邮箱">`，对应修改闭合标签。
- 经历与论文：当前标记为“待补充”，请替换为真实信息。新增条目可复制相应的 `article`。中英文同时添加对应字典键。
- 项目、论文链接：填写真实 URL，不使用 `href="#"` 伪链接；本地资源使用 `./assets/...` 相对路径。
- 配色：修改 CSS 开头的 `:root` 变量。字体使用 系统字体：英文 Times New Roman，中文正文宋体（Songti SC / SimSun），标题楷体（Kaiti SC / KaiTi），缺失时回退至衬线字体。

## GitHub Pages 部署

项目仓库：https://github.com/supremewen666/supremewen666.github.io

1. 在仓库 **Settings → Pages → Build and deployment → Source** 选择 **GitHub Actions**。
2. 在 **Actions** 中运行 `Deploy personal website to GitHub Pages`，或推送到 `main` 自动部署。
3. 部署成功后访问 https://supremewen666.github.io/ 。

工作流只发布 `index.html` 和 `assets/`，不会发布 README 或开发文件。

`sprw.github.io` 是页面品牌名称。GitHub Pages 默认域名由账号决定：这个仓库对应 `supremewen666.github.io/`。要使用 `https://sprw.github.io/`，需要拥有 `sprw` GitHub 账号及其 `sprw.github.io` 仓库。不要将 `sprw.github.io` 写入 CNAME；它不是当前账号可任意绑定的自定义域名。

GitHub 官方说明：https://docs.github.com/en/pages/getting-started-with-github-pages/what-is-github-pages

## 本地预览

```sh
python3 -m http.server 8000
```

打开 http://localhost:8000 。
