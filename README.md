# 🌐 zhuu.top 个人品牌门户项目

这是我的个人网站项目，通过 AI 辅助开发流程，构建了一个高性能、自动化部署的展示平台。

## 📋 项目概况
- **域名:** [zhuu.top](https://zhuu.top)
- **网站定位:** 个人信息展示、项目索引、Hobby 展示
- **部署状态:** ✅ 全球已上线 (Vercel Hosted)
- **实名状态:** ✅ 腾讯云已过审，解析正常

## 🛠️ 技术架构与配置备忘

### 1. 开发环境：Cursor (AI-Native IDE)
- **开发模式:** 使用 Cursor 的 `Build with Agent` 功能，通过自然语言对话生成 HTML/CSS。
- **UI 风格:** 采用极简主义、苹果风高级感设计，支持移动端自适应与玻璃拟态视觉效果。

### 2. Git 环境配置（身份标识）
为了确保提交记录显示正确的身份，已在本地执行以下全局配置：
- **用户名:** `Zhuziqing202`
- **邮箱:** `2206603382@qq.com`
- **常用指令:**
  - 查看配置: `git config --global user.name` / `git config --global user.email`
  - 修改用户名: `git config --global user.name "Zhuziqing202"`
  - 修改邮箱: `git config --global user.email "2206603382@qq.com"`

### 3. SSH 密钥与网络通信（网络故障解决）
在配置过程中遇到了 GitHub 22 端口连接超时 (Connection timed out) 的问题，已通过 **SSH over HTTPS (443端口)** 成功解决。

- **密钥生成（示例）:**
```
ssh-keygen -t rsa -b 4096 -C "2206603382@qq.com"
```
- **密钥路径（示例）:**
  - 私钥: `C:\Users\Zhu\.ssh\id_rsa`
  - 公钥: `C:\Users\Zhu\.ssh\id_rsa.pub`

- **SSH 配置文件示例（~/.ssh/config）**
```
Host github.com
  Hostname ssh.github.com
  Port 443
  User git
  IdentityFile C:\Users\Zhu\.ssh\id_rsa
```

> 说明：将上述路径与用户名替换为你本地实际值。Windows 上可使用 `notepad %USERPROFILE%\\.ssh\\config` 编辑配置文件。

### 4. 部署与托管
- 本站通过 Vercel 托管，使用静态站点部署（仅 HTML/CSS/静态资源）。
- 若需更新：将变更推送到 Git 仓库后，Vercel 会根据设定自动触发部署。

## 🚀 本地预览
- 直接在浏览器中打开项目根目录下的 [index.html](index.html) 即可预览：

```sh
# 在文件管理器中双击 index.html，或使用一个简单的本地服务器：
python -m http.server 8000
# 然后在浏览器打开 http://localhost:8000/
```

## ✅ 常用 Git 操作（示例）
```sh
git status
git add .
git commit -m "chore: update site"
git push origin main
```

## 贡献与改进建议
- 若你想帮我改进页面样式、加入新模块或优化无障碍支持，欢迎提交 PR 或在仓库中发起 issue。

---
版权所有 © 2026 朱子青。
