# 爱旅游的AI小白｜网站使用与免费上线指南

## 1. 先预览成品

下载压缩包并解压，双击 `index.html` 就可以用浏览器查看网站。电脑和手机都能访问上线后的网站。网站已换成统一风格的旅行与科技主题图片；图片为网站视觉素材，不代表你的真实拍摄作品。

## 2. 修改属于你的内容

- 用记事本或 VS Code 打开 `content.js`，修改 `SITE_CONTENT.photos` 中的标题、地点、描述和 `image` 图片地址。
- 把你自己的照片（建议 JPG 或 WebP，单张尽量小于 1MB）复制进 `assets` 文件夹，例如 `assets/my-sunset.jpg`，然后把对应 `image` 改成 `assets/my-sunset.jpg`。
- 修改 `SITE_CONTENT.aiArticles` 和 `SITE_CONTENT.techArticles` 可更新文章。每篇文章的 `body` 中，每一段用英文逗号分隔的引号字符串表示。
- 要修改首页介绍、关于我文字、微信公众号名称等，请用编辑器打开 `index.html` 并搜索对应文字替换。
- `style.css` 控制颜色、排版；`script.js` 控制菜单、筛选和弹窗。不懂代码可以先不修改它们。
- 修改完后刷新 `index.html` 检查，确认无误再上传。

**提醒：** 这个版本是无需数据库的静态个人网站，文章需要编辑文件后上传，不包含后台登录、在线发布编辑器、评论区或照片云同步。

## 3. 当前网站地址

已发布地址：[https://ai-travel-blog.neat-ray-3949.chatgpt.site](https://ai-travel-blog.neat-ray-3949.chatgpt.site)

## 4. 免费发布到 GitHub Pages（备用方案）

1. 打开 https://github.com 注册并登录账号，完成邮箱验证。
2. 点击右上角 `+` → `New repository`（新建仓库）。
3. 在仓库名称填写 `ai-travel-blog`，选择 **Public**（公开），创建仓库。**不要上传私人信息、密码、未获授权的公司材料。**
4. 进入仓库，点击 `Add file` → `Upload files`，把解压后文件夹**内部的** `index.html`、`style.css`、`content.js`、`script.js` 和整个 `assets` 目录的文件上传（包含 JPG 图片和 SVG 图标）。
5. 点击页面底部的 `Commit changes`（提交更改）。确认仓库根目录能看到 `index.html`，且 `assets` 内的图片存在。
6. 点击仓库 `Settings` → 左边 `Pages`。
7. 在 `Build and deployment` 的 `Source` 选 `Deploy from a branch`；`Branch` 选 `main`，文件夹选 `/(root)`，点击 `Save`。
8. 部署完成后，打开 `https://你的GitHub用户名.github.io/ai-travel-blog/`。如果刚发布显示 404，稍后刷新，并回到 `Settings → Pages` 查看部署状态（官方文档说明发布可能需要最多约 10 分钟）。
9. 如需更新网站，在 GitHub 仓库上传修改后的同名文件并提交；GitHub Pages 会自动重新部署。

**重要**：如果你将仓库命名为 `你的GitHub用户名.github.io`，站点地址则是 `https://你的GitHub用户名.github.io/`，不带 `/ai-travel-blog/`。

## 5. 常见问题

- **图片显示不出来**：检查 `content.js` 中的 `image` 路径大小写和扩展名，与 `assets` 实际文件名是否一致。GitHub 对大小写敏感。
- **404 页面**：检查 `index.html` 是否在仓库根目录、Pages 是否选 main/(root)、发布是否完成。
- **手机菜单打不开**：检查 `script.js` 是否上传。
- **页面没有样式**：检查 `style.css` 是否在根目录。
- **打开网站慢**：本站主体内容与图片在本地文件夹，字体通过 Google Fonts 在线加载；字体无法访问时会自动使用系统字体。中国大陆网络访问 GitHub Pages 的稳定性因网络环境而异。

## 6. 进一步升级思路

当文章多起来时，可以以后升级为支持 Markdown 或后台编辑的博客系统；当前版本的重点是免费、简单、设计美观、不用购买服务器。

官方参考：
- https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site
- https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site


