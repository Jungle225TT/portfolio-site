# 姜亭汀 — Digital Garden 个人主页

## 项目简介

产品经理/技术项目管理 求职作品集网站，采用「数字花园」主题设计（自然 + 科技），深色森林配色。

## 项目结构

```
portfolio-site/
├── index.html                     # 主页（首页）
├── README.md                      # 项目说明
├── assets/
│   └── images/
│       ├── avatar.png             # 个人照片
│       └── sign-in.png            # 智能工单项目封面图
└── pages/
    ├── project-pawfly.html        # PawFly 项目详情页
    ├── project-monopoly.html      # 大富翁游戏项目详情页
    ├── project-ticket.html        # 智能工单管理平台详情页
    └── project-portfolio.html     # 多语言作品集网站详情页
```

## 主页功能模块

1. **Hero 开屏** — 粒子动画背景 + 鼠标追踪光晕
2. **关于我** — 个人照片（有机形状动画）+ 简介 + 标签 + 统计数据
3. **项目作品集** — 4 个项目卡片，点击可跳转到独立详情页
4. **技能树** — 6 个分类卡片展示技术栈
5. **AI 数字分身** — 接入 Claude API 的聊天机器人（需配置 API）
6. **联系方式** — 邮箱、电话、位置信息

## 项目详情页

每个项目详情页包含以下板块（可自定义编辑）：

- **项目概述** — 背景与目标描述 + 截图占位
- **核心功能** — 4 个功能亮点卡片
- **设计展示** — 2×2 图片网格（可上传设计稿）
- **项目成果** — 总结与收获

## 如何使用

### 本地预览

直接用浏览器打开 `index.html` 即可预览。

> 注意：AI 聊天功能需要网络环境才能调用 Claude API。

### 编辑内容

1. 用 VS Code / Cursor 打开整个 `portfolio-site` 文件夹
2. 编辑 `pages/` 下的各项目详情页，替换占位文字和图片
3. 添加新的项目封面图到 `assets/images/` 目录

### 添加项目封面图

在各项目卡片中替换封面图：

1. 将图片放入 `assets/images/`
2. 在 `index.html` 中找到对应的 `project-preview` 区块
3. 替换占位内容为 `<img class="project-cover" src="assets/images/你的图片.png" alt="描述">`

### 部署到阿里云

将整个 `portfolio-site` 文件夹上传到服务器的 Web 根目录即可。

## 技术栈

- HTML5 / CSS3 / JavaScript（纯前端，无框架依赖）
- Google Fonts（Playfair Display + DM Sans + JetBrains Mono + Noto Serif SC）
- Claude API（AI 聊天功能）
- CSS 动画（粒子背景、滚动渐现、有机形状变形）

## 自定义配色

所有颜色通过 CSS 变量管理，在 `index.html` 的 `:root` 中统一修改：

```css
:root {
  --green-deep: #1a3a2a;
  --green-light: #52b788;
  --blue-dark: #1b2d4f;
  --bg-primary: #0a1a12;
  /* ... 更多变量 */
}
```
