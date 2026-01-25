# 朱子青的个人网站

一个现代、简约、响应式的个人单页网站，展示心理学背景、科研项目、技术探索和多元兴趣。

## 📁 项目结构

```
网页/
├── index.html                    # 主页（单页网站，包含所有主要板块）
├── README.md                     # 项目说明（这个文件）
│
├── projects/                     # 作品与技术部分
│   ├── research-1.html          # 科研项目 #1 详情页
│   ├── research-2.html          # 科研项目 #2 详情页
│   ├── tech-1.html              # 技术项目 #1 详情页
│   └── tech-2.html              # 技术项目 #2 详情页
│
├── pages/                        # 关于我部分
│   ├── thoughts.html            # 我的思考（人生哲学与自洽）
│   └── learning-notes.html      # 学习笔记（心理学相关）
│
├── interests/                    # 兴趣魔盒（四个兴趣板块）
│   ├── travel.html              # 极限旅行（旅游与公共交通）
│   ├── gadgets.html             # 数码折腾（硬件与设备折腾）
│   ├── architecture.html        # 古建筑入门（建筑史与工艺）
│   └── aerospace.html           # 航空航天（飞行与太空探索）
│
└── travel/                       # 原始城市页面（可选保留）
    ├── beijing.html
    ├── shanghai.html
    ├── chengdu.html
    ├── guangzhou.html
    └── hangzhou.html
```

## 🎨 设计系统与美学

### 色彩系统
在每个 HTML 文件的 `<style>` 中都定义了统一的 CSS 变量：

```css
:root {
  --color-bg: #fafbfc;           /* 浅灰背景 */
  --color-card: #ffffff;          /* 白色卡片 */
  --color-text: #1a202c;          /* 深灰文本 */
  --color-text-light: #718096;    /* 浅灰辅助文本 */
  --color-border: #e2e8f0;        /* 边框浅灰 */
  --color-accent: #4f46e5;        /* 紫色强调色 */
  --color-accent-light: #eef2ff;  /* 强调色浅背景 */
}
```

### 间距系统
- `--sp-xs: 4px`   - 微小间距
- `--sp-sm: 8px`   - 小间距
- `--sp-md: 16px`  - 标准间距
- `--sp-lg: 24px`  - 大间距
- `--sp-xl: 32px`  - 更大间距
- `--sp-2xl: 48px` - 最大间距

### 圆角与阴影
- **圆角**：sm (8px), md (12px), lg (16px), xl (20px)
- **阴影**：sm, md, lg 三个深度，提供微妙的深度感
- **过渡**：fast (150ms), base (250ms) 保证动画流畅

## 📝 核心特性

### 1. 极简主义设计
- 大量留白，不过度装饰
- 清晰的视觉层级
- 强调内容而非形式

### 2. 柔和过渡动画
- 卡片悬停上升效果
- 颜色平滑过渡
- 渐变背景动画

### 3. 响应式布局
- **桌面端 (>768px)**：多栏网格，充分利用空间
- **平板端 (768px)**：调整列数，优化可读性
- **手机端 (<480px)**：单栏布局，最大化内容宽度

### 4. 语义化 HTML
- 清晰的页面结构
- 易于SEO和可访问性
- 便于维护和扩展

## 🔧 如何维护和修改

### 修改主页内容

主页 `index.html` 分为以下主要部分，你可以轻松编辑：

#### 头部导航
```html
<header>
  <div class="header-content">
    <a href="#" class="logo">朱子青</a>
    <nav>
      <!-- 修改导航链接 -->
    </nav>
  </div>
</header>
```

#### Hero Section（欢迎层）
```html
<section class="hero">
  <h1>心理学、探索与自洽</h1>
  <p class="subtitle">修改这里的副标题...</p>
  <div class="cta-buttons">
    <!-- 修改 CTA 按钮 -->
  </div>
</section>
```

#### Projects Section（作品与技术）
找到 `<section id="projects">` 并修改：
- 每个项目卡片的标题、描述和链接
- 改变图标（修改 `<div class="project-icon">`）
- 更新项目链接路径

#### About Section（关于我）
找到 `<section id="about">` 并修改：
- 左侧的个人哲学文本
- 右侧的两个跳转链接（思考、笔记）
- 添加更多个人信息

#### Interests Section（兴趣魔盒）
找到 `<section id="interests">` 并修改：
- 四个兴趣卡片的标题和描述
- 兴趣的emoji表情
- 链接指向

#### Footer
```html
<footer>
  <!-- 修改备案信息 -->
  <!-- 修改社交链接 -->
</footer>
```

### 修改详情页面

每个项目/兴趣的详情页面（如 `projects/research-1.html`）结构一致：

**必改项**：
1. `<title>` 标签 - 浏览器标签显示
2. `<h1 class="page-title">` - 页面标题
3. `.page-meta` - 发布时间、标签等
4. `.highlight-box` - 项目摘要
5. `.content-section` - 多个内容区块

**占位符替换**：
- 找到 `【在这里...】` 的所有地方
- 替换为你的真实内容
- 删除不需要的 section

**示例**：
```html
<!-- 替换前 -->
<h2>项目背景</h2>
<p>【在这里详细说明你为什么开始这个项目...】</p>

<!-- 替换后 -->
<h2>项目背景</h2>
<p>这个项目源于我在心理学研究中发现的一个有趣现象...</p>
```

### 添加图片

将占位符替换为真实图片：

```html
<!-- 替换前 -->
<div class="image-placeholder">
  [项目相关的图片、图表或可视化内容]
</div>

<!-- 替换后 -->
<div class="image-placeholder">
  <img src="./images/my-project.jpg" alt="项目展示图">
</div>
```

### 添加新页面

如果要添加新的项目或兴趣：

1. **复制现有页面**
   - 参考 `projects/research-1.html` 的结构
   - 复制为新文件（如 `projects/research-3.html`）

2. **修改页面内容**
   - 更新 `<title>`
   - 更改 `<h1>` 和所有占位符
   - 添加你的具体内容

3. **在主页添加链接**
   - 在 `index.html` 的对应 section 中添加新卡片
   - 更新链接指向新页面

**示例**：
```html
<!-- 在 index.html 的 projects-grid 中添加 -->
<a href="./projects/research-3.html" class="project-card">
  <div class="project-icon">🔍</div>
  <h3>科研项目 #3</h3>
  <p>你的新项目描述</p>
  <div class="project-arrow">了解更多 →</div>
</a>
```

## 🎨 样式定制

### 改变整体颜色主题

在 `index.html` 的 `:root` 中改变 `--color-accent`：

```css
:root {
  --color-accent: #4f46e5;  /* 现在是紫色，改这里 */
}
```

推荐的替代颜色：
- `#0ea5e9` - 天蓝色
- `#10b981` - 翡翠绿
- `#f59e0b` - 琥珀黄
- `#ef4444` - 红色
- `#8b5cf6` - 深紫

**重要**：记得在所有文件中保持颜色一致。

### 修改字体

在 `body` 的 `font-family` 中修改：
```css
body {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', ...;
}
```

替代方案：
- `'Noto Sans SC'` - 思源黑体（中文更舒适）
- `'FZSJ-QZCSXS'` - 方正喜鹊黑（古香古色）
- 任何 Google Fonts 中的字体

### 调整间距和大小

修改 CSS 变量即可影响整个网站：
```css
:root {
  --sp-lg: 24px;  /* 改为 20px 会更紧凑 */
  --sp-xl: 32px;  /* 改为 40px 会更宽松 */
}
```

## 📋 维护清单

### 初始设置（必须）
- [ ] 替换 `your-email@example.com` 为真实邮箱
- [ ] 更新 GitHub 链接
- [ ] 更新小红书链接或二维码
- [ ] 修改页脚的备案信息

### 内容完善（强烈建议）
- [ ] 完成四个项目详情页的内容
- [ ] 完成两个"关于我"页面的内容
- [ ] 完成四个兴趣页面的详细描述
- [ ] 添加真实的项目图片

### 定期更新（维持活力）
- [ ] 添加新的项目
- [ ] 更新旅行记录
- [ ] 补充学习笔记
- [ ] 分享新的想法

## 💡 高级技巧

### 添加搜索功能
虽然是静态网站，但可以添加客户端搜索：
```html
<script src="https://cdn.jsdelivr.net/npm/lunr@2/lunr.min.js"></script>
```

### 添加评论系统
使用免费服务如 Disqus 或 Utterances：
```html
<!-- Utterances 评论系统 -->
<script src="https://utteranc.es/client.js"
  repo="your-username/repo-name"
  issue-term="pathname"
  label="comment"
  theme="github-light"
  crossorigin="anonymous"
  async>
</script>
```

### 添加网站分析
在 `</body>` 前添加 Google Analytics：
```html
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_ID');
</script>
```

### SEO 优化
在每个页面的 `<head>` 中添加：
```html
<meta name="description" content="页面描述">
<meta name="keywords" content="关键词1, 关键词2">
<meta property="og:title" content="分享标题">
<meta property="og:description" content="分享描述">
<meta property="og:image" content="分享图片">
```

## 🚀 部署到网络

### 部署到 GitHub Pages
1. 在 GitHub 创建 `username.github.io` 仓库
2. 将文件上传到仓库
3. 自动生成网站（https://username.github.io）

### 部署到 Vercel
1. 连接 GitHub 仓库
2. 一键部署（自动HTTPS）
3. 绑定自定义域名

### 部署到 Netlify
1. 拖拽文件夹上传
2. 自动生成网址
3. 支持自定义域名和SSL

## ❓ 常见问题

**Q: 如何改变导航菜单颜色？**
A: 找到 `nav a` 的 CSS 规则，改变 `color` 属性即可。

**Q: 如何添加新的兴趣类别？**
A: 在 `interests/` 文件夹创建新 HTML，参照 `travel.html` 结构，在主页添加链接。

**Q: 网站在手机上显示不好怎么办？**
A: 检查是否有 `<meta name="viewport">` 标签，并在浏览器开发者工具中用手机模式测试。

**Q: 如何添加暗黑模式？**
A: 在 CSS 中添加 `@media (prefers-color-scheme: dark)` 规则。

**Q: 页面加载很慢怎么办？**
A: 压缩图片、使用 CDN 加载库文件、删除未使用的 CSS。

## 📚 推荐资源

- [MDN Web 文档](https://developer.mozilla.org) - HTML/CSS 学习
- [Can I Use](https://caniuse.com) - 浏览器兼容性查询
- [CSS Tricks](https://css-tricks.com) - 高级 CSS 技巧
- [Web.dev](https://web.dev) - 网页性能和最佳实践

## 📄 许可证

© 2026 朱子青 | 基于 MIT 协议开源

---

**最后的话**：

这个网站的设计理念是"内容为王"。所有的样式和动画都是为了让你的想法和作品更清晰地呈现。不要过度追求复杂的效果，专注于写出有意义、有深度的内容。

一个简约而诚实的个人网站，往往比充满特效的网站更令人印象深刻。祝你在这个网站上分享更多有趣的想法和项目！
