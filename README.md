# 阿里云推荐计划展示网站

🌐 **专属推荐链接:** https://www.alibabacloud.com/campaign/benefits?referral_code=A92VJ2

---

## 📁 文件结构

```
aliyun-referral/
├── index.html          # 主页面（单页 Landing Page）
├── README.md           # 说明文档
└── assets/             # (可选) 图片等资源
```

---

## 🚀 快速部署

### 方式 1: GitHub Pages (免费推荐)

```bash
# 1. 初始化 Git 仓库
cd /home/admin/.openclaw/workspace/aliyun-referral
git init
git add .
git commit -m "Initial commit - Aliyun referral landing page"

# 2. 推送到 GitHub
git remote add origin https://github.com/Dragons777-cpu/aliyun-referral.git
git push -u origin main

# 3. 启用 GitHub Pages
# 访问：https://github.com/Dragons777-cpu/aliyun-referral/settings/pages
# 选择 main branch，保存
# 获得链接：https://Dragons777-cpu.github.io/aliyun-referral/
```

### 方式 2: Vercel (免费)

```bash
# 1. 安装 Vercel CLI
npm install -g vercel

# 2. 部署
cd /home/admin/.openclaw/workspace/aliyun-referral
vercel

# 3. 按提示操作，获得链接
# 例如：https://aliyun-referral.vercel.app
```

### 方式 3: Netlify (免费)

```bash
# 访问 https://app.netlify.com/drop
# 拖拽 aliyun-referral 文件夹
# 获得链接
```

### 方式 4: 自有服务器

```bash
# 使用 Nginx
sudo cp -r /home/admin/.openclaw/workspace/aliyun-referral /var/www/aliyun-referral

# Nginx 配置
server {
    listen 80;
    server_name your-domain.com;
    root /var/www/aliyun-referral;
    index index.html;
}
```

---

## 📊 网站功能

### 已集成

- ✅ **响应式设计** — 手机/平板/电脑自适应
- ✅ **推荐链接** — 多处嵌入你的专属链接 `A92VJ2`
- ✅ **服务展示** — 6 大服务模块
- ✅ **价格展示** — 3 档价格方案
- ✅ **联系表单** — 潜在客户收集
- ✅ **SEO 优化** — 基础 SEO 标签
- ✅ **动画效果** — 平滑滚动、淡入动画

### 表单处理

当前表单提交后显示成功提示，实际使用可选择：

**方案 A: Email 接收 (推荐)**
```javascript
// 使用 Formspree (免费)
// 注册 https://formspree.io/
// 替换 form action:
<form action="https://formspree.io/f/your-form-id" method="POST">
```

**方案 B: 后端处理**
```javascript
// 发送到你的后端 API
fetch('/api/contact', {
    method: 'POST',
    body: JSON.stringify(data)
});
```

**方案 C: Google Sheets**
```javascript
// 使用 Google Apps Script
// 表单数据自动存入 Google Sheets
```

---

## 🎨 自定义修改

### 修改推荐链接

```html
<!-- 搜索并替换所有 A92VJ2 -->
https://www.alibabacloud.com/campaign/benefits?referral_code=A92VJ2
```

### 修改价格

```html
<!-- 在 index.html 中找到 pricing 部分 -->
<div class="price">¥2000<span>/项目</span></div>
<!-- 修改为你的价格 -->
```

### 修改联系方式

```html
<!-- 在 footer 部分添加你的联系方式 -->
<p>微信：your-wechat-id</p>
<p>Email: your@email.com</p>
```

---

## 📈 推广建议

### 1. GitHub

```markdown
# 在 GitHub Profile 添加
[☁️ 阿里云云服务咨询](https://your-site.com)
```

### 2. LinkedIn

```
发布技术文章，文末添加：
需要阿里云云服务咨询？访问：https://your-site.com
```

### 3. Twitter/X

```
发推系列：
"阿里云 vs AWS：跨境业务怎么选？🤔
完整对比 + 专属优惠：https://your-site.com
#阿里云 #云服务 #跨境"
```

### 4. 技术博客

```
写教程文章：
- "如何用阿里云搭建跨境电商网站"
- "阿里云 ECS 新手完全指南"
- 文末添加推荐链接
```

---

## 📊 追踪统计

### 添加 Google Analytics

```html
<!-- 在 </head> 前添加 -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

### 添加链接点击追踪

```javascript
// 在 index.html 的 script 部分添加
document.querySelectorAll('a[href*="referral_code"]').forEach(link => {
    link.addEventListener('click', function() {
        // 发送到分析服务
        gtag('event', 'click', {
            'event_category': 'referral',
            'event_label': 'aliyun_signup'
        });
    });
});
```

---

## 🔧 后续优化

### 可以添加的功能

- [ ] 在线客服聊天 (Tawk.to 免费)
- [ ] 客户案例展示
- [ ] 博客/文章系统
- [ ] 在线预约日历
- [ ] 多语言支持 (EN/CN)
- [ ] A/B 测试优化转化率

### SEO 优化

- [ ] 添加更多关键词
- [ ] 创建博客内容
- [ ] 获取外部链接
- [ ] 提交到搜索引擎

---

## 📞 技术支持

如有问题，请联系：
- Email: your-email@example.com
- 微信：your-wechat-id

---

**创建时间:** 2026-04-08  
**版本:** 1.0.0  
**状态:** ✅ 已完成，可立即部署
