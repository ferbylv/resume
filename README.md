# 吕洋个人介绍网站

这是一个纯静态个人介绍网站，已经可以直接部署到 GitHub Pages。

## 本地预览

在项目根目录运行：

```bash
python3 -m http.server 4173
```

然后打开 `http://localhost:4173`。

## 文件说明

- `index.html`：页面结构
- `styles.css`：视觉样式与响应式布局
- `script.js`：滚动显现和年份脚本
- `assets/luyang-resume.pdf`：简历下载文件
- `assets/favicon.svg`：站点图标
- `.nojekyll`：避免 GitHub Pages 用 Jekyll 处理静态资源

## 部署到 GitHub Pages

### 方式一：仓库根目录直接发布

1. 在 GitHub 创建一个新仓库。
2. 把当前目录内容推送到仓库：

```bash
git init
git add .
git commit -m "feat: add personal portfolio site"
git branch -M main
git remote add origin https://github.com/<你的用户名>/<仓库名>.git
git push -u origin main
```

3. 打开 GitHub 仓库页面，进入 `Settings` -> `Pages`。
4. 在 `Build and deployment` 中选择 `Deploy from a branch`。
5. `Branch` 选择 `main`，目录选择 `/ (root)`，保存。
6. 等待几十秒到几分钟，GitHub 会生成访问地址。

### 访问地址规则

- 如果仓库名是 `<你的用户名>.github.io`，访问地址通常是：

```text
https://<你的用户名>.github.io/
```

- 如果是普通仓库，比如 `jianli-site`，访问地址通常是：

```text
https://<你的用户名>.github.io/jianli-site/
```

## 自定义内容

- 要修改文案：编辑 `index.html`
- 要修改颜色和布局：编辑 `styles.css`
- 要替换简历：直接替换 `assets/luyang-resume.pdf`

所有链接都使用相对路径，所以无论是用户主页仓库还是项目仓库，都可以正常部署。
