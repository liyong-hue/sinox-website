# PUSKILL.com 网站完整结构分析报告

> 分析日期：2026-07-01
> 目标网站：https://www.puskill.com
> 建站平台：WordPress + 8Theme/XStore 主题 + WooCommerce
> 所属公司：Shenzhen Xinshenhua Technology Co., Ltd.（深圳鑫申华科技有限公司）
> 品牌：PUSKILL

---

## 一、导航栏结构

### 一级菜单（从左到右）

| 序号 | 菜单名称 | URL | 说明 |
|------|---------|-----|------|
| 0 | Logo（图标） | / | 网站 Logo，点击返回首页 |
| 1 | Home | / | 首页 |
| 2 | Products | /products/ | 产品列表页（WooCommerce 商店） |
| 3 | Application | /application/ | 产品应用场景展示页 |
| 4 | About us | /about-us/ | 关于我们/公司介绍 |
| 5 | News | /news/ | 新闻/博客文章列表 |
| 6 | Help | /help/ | 帮助中心/安装教程 |
| 7 | Video | /video/ | 视频展示页 |
| 8 | Contacts | /contact-us/ | 联系我们 |

### 导航栏右侧功能区

| 功能 | 说明 |
|------|------|
| Search | 搜索图标按钮，点击展开搜索输入框 |
| Login / Sign in | 用户登录入口（/my-account/），弹出登录表单 |
| Register | 用户注册入口（/wp-login.php?action=register） |

### 导航栏二级菜单

该网站导航栏**无传统下拉二级菜单**。所有菜单项均为一级直达链接。产品分类通过侧边栏和页面内部区块展示。

---

## 二、首页板块结构（从上到下）

### 板块 1：Hero 轮播图区

- **类型**：全宽幻灯片轮播（Revolution Slider）
- **内容**：品牌形象大图，含产品展示
- **交互**：左右切换箭头、READ MORE 按钮
- **数量**：多张轮播（至少 3 张）

### 板块 2：Product Categories（产品大类入口）

- **标题**：Product Categories
- **描述**："Products are categorized into Computer Hardware, including Memory Modules and Solid State Drives."
- **内容**：两张大卡片
  - **RAM** 卡片 → 带 READ MORE 按钮
  - **SSD** 卡片 → 带 READ MORE 按钮
- **用途**：引导用户进入两大核心产品线

### 板块 3：Featured Products（精选产品展示）

- **标题**："Explore our featured products, offering top-quality performance and innovation."
- **布局**：多排产品卡片网格（桌面端约 4 列）
- **每个产品卡片包含**：
  - 产品缩略图
  - 分类标签（Computer Hardware / RAM / SSD）
  - 产品名称
  - 价格区间（部分产品显示，如 $29.00 – .00）
  - Read more 或 Select options 按钮
  - Quick View 快速查看功能
- **产品类型覆盖**：DDR3/DDR4/DDR5 台式/笔记本内存、SSD（NVMe/SATA）等

### 板块 4：About us（公司简介）

- **标题**：About us
- **内容**：公司简介文本（约 150 词）
  - Founded in 2017, Shenzhen Xinshenhua Technology
  - 核心团队自 2008 年起从事存储行业
  - 自有品牌 PUSKILL
  - 产品线：DDR ICs, DRAM modules (DDR3/DDR4/DDR5), SSDs
  - 研发生产基地：深圳、香港、美国
  - ISO 9001 质量体系
- **CTA**：READ MORE 按钮

### 板块 5：Our News（新闻/博客）

- **标题**："Stay updated with the latest news and updates from us."
- **布局**：博客文章列表（3 列卡片式布局）
- **每篇文章包含**：
  - 特色图片
  - 分类标签（如 ddr3 laptop memory）
  - 文章标题
  - 发布日期（如 June 30, 2026）
  - 评论数
  - 文章摘要
  - Continue reading 链接
- **分页**：Showing 1–3 of 10 posts（共 10 篇，分 4 页）
- **作者**：xinshenhua

### 板块 6：Qualification Certificate（资质认证）

- **标题**：QUALIFICATION CERTIFICATE
- **描述**："PUSKILL follows ISO 9001, ensuring strict material inspection, efficient production, and stable quality, with certifications including ROHS, CE, and FCC."
- **内容**：多张认证证书轮播展示（ROHS、CE、FCC 等）
- **交互**：左右切换箭头、底部指示点

### 板块 7：Get in Touch（联系方式）

- **标题**：get in touch
- **内容**：
  - 公司全称：Shenzhen Xinshenhua Technology Co.,ltd
  - 地址：602, Bldg.2, No.9, East Zone, Shangxue Tech. Park, Xinxue Community, Bantian Subdistrict, Longgang Dist.
  - 电话：86-0755-28289902 / +86 13242930281
  - 邮箱：info@puskill.com
- 无联系表单（联系表单在首页其他位置）

---

## 三、产品分类体系

### 整体架构

产品统一归类在 **Computer Hardware** 大分类下，下设两个子分类：

`
Computer Hardware
├── RAM (Memory Modules)
│   ├── DDR3
│   │   ├── DDR3 Desktop RAM (1.5V)
│   │   ├── DDR3 Laptop RAM (DDR3L 1.35V / PC3-12800S)
│   │   └── DDR3 for Gaming PC
│   ├── DDR4
│   │   ├── DDR4 Desktop RAM (UDIMM, OEM/Factory)
│   │   ├── DDR4 Laptop RAM (SODIMM)
│   │   ├── DDR4 Gaming RAM (Heatsink/高性能)
│   │   └── DDR4 RGB RAM
│   └── DDR5
│       ├── DDR5 Desktop RAM
│       ├── DDR5 Laptop RAM (SODIMM)
│       ├── DDR5 Gaming RAM (Heatsink/6000MHz)
│       ├── DDR5 ECC Server RAM
│       └── DDR5 Desktop 8GB
└── SSD (Solid State Drives)
    ├── M.2 NVMe PCIe 4.0 SSD (128GB–2TB)
    ├── M.2 NVMe PCIe 3.0 SSD (Top Seller, 128GB–2TB)
    ├── M.2 PCIe NVMe 2280 SSD 3.0
    ├── M.2 SATA SSD
    ├── 2.5 Inch SATA3 SSD (120GB–2TB)
    └── Internal SATA SSD Drive
`

### 产品列表页功能（/products/）

| 功能 | 选项 |
|------|------|
| 面包屑导航 | Home > Return to previous page |
| 排序方式 | Default sorting / Sort by popularity / Sort by average rating / Sort by latest |
| 视图切换 | Grid（网格）/ List（列表） |
| 每页显示 | 12 / 24 / 36 / All |
| 侧边栏分类 | Computer Hardware > RAM, SSD |
| 分页 | 共 13 页 |
| 价格筛选 | 按价格区间筛选（WooCommerce 原生） |

---

## 四、产品详情页结构

以 DDR3 4GB 8GB 1333MHz 1600MHz Memory ram 产品页为例：

### 页面布局

| 区域 | 内容 |
|------|------|
| **面包屑导航** | Home > Computer Hardware > RAM > 返回上一页 |
| **产品图片区** | 主图 + 缩略图画廊（约 4-5 张图片），支持轮播切换 |
| **产品标题** | 完整 SEO 标题 |
| **分类标签** | Computer Hardware, RAM |
| **产品描述 Tab** | 默认选中 Description 标签页，包含：特点介绍（稳定性能、广泛兼容、即插即用）、详细图片说明 |
| **评价 Tab** | Reviews (0) - WooCommerce 评价系统 |
| **价格** | 部分产品显示价格区间（如 $29.00 – .00），部分不显示公开价格 |
| **购买按钮** | Select options（多变体产品）/ Read more（单产品） |
| **相关产品区** | Related Products 轮播，展示多个同类产品 |

### 特点

- 使用 WooCommerce 产品模板
- 产品图片支持缩放/灯箱效果
- 多变体产品（如不同容量/频率）使用 Select options 按钮
- 无 SKU 公开展示
- 无库存状态显示

---

## 五、页脚结构

### 页脚布局（4 列）

| 列 | 标题 | 内容 |
|----|------|------|
| 第 1 列 | 公司信息 | Shenzhen Xinshenhua Technology Co., Ltd. 简介 + 产品链接（Computer Hardware / RAM / SSD） |
| 第 2 列 | QUICKLINKS | HOME / APPLICATION / About us / NEWS / FAQ / Video / Contact us |
| 第 3 列 | CONTACTS | Email: info@puskill.com / Phone: +86-0755-28289902 / WhatsApp: +86 13242930281 / Address |
| 第 4 列 | 社交媒体 | Facebook / LinkedIn / TikTok / X / Instagram / YouTube（图标链接） |

### 页脚底部栏

| 元素 | 内容 |
|------|------|
| 版权信息 | Copyright 2026 Shenzhen Xinshenhua Technology Co., Ltd. |
| 隐私政策 | Privacy Policy 链接 |
| 语言选择器 | 下拉菜单（English / Japanese / Korean / Portuguese / Russian / Spanish） |
| 移动端菜单 | Home / Shop / Contact us / More |

### 浮动元素（全局）

| 元素 | 说明 |
|------|------|
| Chaty 在线客服 | 右下角浮动聊天按钮，支持 WhatsApp、Phone、Email 等渠道 |
| 回到顶部 | 无独立按钮（主题可能内置） |

---

## 六、其他子页面详情

### Application 页面（/application/）

- 展示产品应用场景
- 侧边栏：Computer Hardware > RAM / SSD
- 内容较简洁，以图文展示不同应用领域

### About us 页面（/about-us/）

- 公司详细介绍
- 品牌合作/客户 Logo 轮播（7 个客户/合作伙伴 Logo）
- 数据统计区：显示关键数字（如年数、产品数、客户数等）
- 双轮播展示

### News 页面（/news/）

- 博客文章列表，每页显示多篇
- 分页导航
- 侧边栏：分类筛选、搜索
- 文章包含：ddr3 laptop memory, sata m.2 ssd, 2tb ssd drive, m.2 sata ssd, internal sata ssd drive, DDR4 desktop memory module, DDR3 for gaming PC, DDR5 server memory manufacturer 等 SEO 文章

### Help 页面（/help/）

- HELP CENTER 标题
- 6 个帮助卡片（图文）：
  - D3 Laptop - Installation and Usage Tutorial
  - D4 Laptop - Installation and Usage Tutorial
  - D5 Laptop - Installation and Usage Tutorial
  - D3 Desktop - Installation and Usage Tutorial
  - D4 Desktop - Installation and Usage Tutorial
  - D5 Desktop - Installation and Usage Tutorial
- 侧边栏：Categories（News）/ Search

### Video 页面（/video/）

- 视频展示页，多个视频卡片
- 用于产品安装教程/评测视频

### Contact us 页面（/contact-us/）

- 公司联系信息（地址、电话、WhatsApp、邮箱、微信、联系人）
- 社交媒体链接（Facebook / Twitter / Instagram / LinkedIn / TikTok / YouTube）
- 无联系表单（联系表单在首页）

---

## 七、整体设计风格分析

### 配色方案

| 元素 | 颜色 | 色值 |
|------|------|------|
| 页面背景 | 浅灰白 | #F7F9FA (rgb 247,249,250) |
| 导航栏背景 | 透明/白色 | 	ransparent / #FFFFFF |
| 正文文字 | 深灰/黑 | gb(0,0,0) / #000000 |
| 页脚文字 | 浅灰 | gb(224,224,224) / #E0E0E0 |
| 按钮背景 | 深灰 | gb(85,85,85) / #555555 |
| 按钮文字（outline风格） | 白色 | #FFFFFF |
| 链接默认色 | 黑色 | #000000 |
| 强调色（价格等） | 橙红 | gb(255,69,0) / #FF4500 (Orangered) |

### 字体

- **主字体**：Rajdhani, sans-serif（Google Fonts - 现代无衬线字体）
- **标题字体**：Rajdhani, sans-serif（与正文相同）
- **风格**：几何化、简洁现代，适合科技/硬件类品牌

### 按钮风格

- **样式**：扁平化设计，无边角圆角（border-radius: 0）
- **尺寸**：padding 约 10.5px 30.8px
- **字号**：约 11.9px - 14px
- **效果**：outline/透明背景 + 白字，hover 时可能有背景色变化
- **分类**：
  - READ MORE 按钮（透明底白字/灰底白字）
  - Select options 按钮（多变体产品）
  - Log in / Register 按钮（灰底浅灰字）
  - Quick View 快速查看（悬停时显示在产品图上）

### 整体风格定性

- **极简工业风**：大量留白、克制配色、几何化字体
- **B2B 外贸风格**：面向全球采购商，强调认证和工厂实力
- **WooCommerce 标准布局**：产品网格 + 侧边栏筛选
- **移动端响应式**：底部固定导航菜单（Home / Shop / Contact us / More）

---

## 八、SINOX 网站可能缺失的板块（对比参考）

基于以上分析，以下是 puskill.com 拥有但可能 SINOX 当前缺失的功能/板块：

| 序号 | 板块/功能 | 重要度 | 说明 |
|------|-----------|--------|------|
| 1 | **Hero 全宽轮播图** | 高 | 首页顶部品牌形象大图轮播，带 CTA 按钮 |
| 2 | **Product Categories 入口卡片** | 高 | 首页大分类引导卡片（RAM/SSD），引导用户进入产品线 |
| 3 | **Quick View 快速查看** | 中 | 产品卡片悬停时快速查看弹窗 |
| 4 | **资质认证展示区** | 高 | ROHS/CE/FCC/ISO 证书轮播展示，增强信任 |
| 5 | **Help 帮助中心** | 中 | 按产品类型（D3/D4/D5 Laptop/Desktop）分类的安装教程 |
| 6 | **Video 视频专区** | 中 | 独立的视频展示页面 |
| 7 | **Chaty 在线客服** | 高 | WhatsApp/Email/Phone 多渠道浮动客服按钮 |
| 8 | **Application 应用场景页** | 中 | 展示产品在不同场景（办公/游戏/服务器等）的应用 |
| 9 | **多语言切换** | 高 | 支持 6 种语言（英/日/韩/葡/俄/西） |
| 10 | **产品多变体价格显示** | 中 | 价格区间展示（如 .00 - .00）+ Select options |
| 11 | **侧边栏产品分类筛选** | 中 | 产品列表页左侧分类 + 排序 + 每页数量选择 |
| 12 | **博客/SEO 文章区** | 高 | 按产品关键词撰写的 SEO 文章（对搜索引擎引流至关重要） |
| 13 | **社交媒体全面覆盖** | 中 | Facebook/LinkedIn/TikTok/X/Instagram/YouTube 六平台 |
| 14 | **页脚完整信息架构** | 高 | 四列页脚：公司信息 + 快速链接 + 联系方式 + 社交媒体 |
| 15 | **Grid/List 视图切换** | 低 | 产品列表的网格/列表视图切换 |

---

## 九、技术栈识别

| 层面 | 技术 |
|------|------|
| CMS | WordPress |
| 主题 | 8Theme - XStore（WooCommerce 电商主题） |
| 电商引擎 | WooCommerce |
| 页面构建器 | Elementor / WPBakery（推测） |
| 幻灯片 | Revolution Slider (SR7) |
| 在线客服 | Chaty |
| 图片格式 | WebP |
| 语言 | PHP（WordPress 后端） |

---

## 十、截图文件清单

所有截图保存在 temp 目录：

| 文件名 | 内容 |
|--------|------|
| puskill-home.png | 首页全页截图 |
| puskill-homepage-full.png | 首页全页截图（products页面） |
| puskill-products.png | Products 产品列表页 |
| puskill-application.png | Application 应用场景页 |
| puskill-about.png | About us 关于我们页 |
| puskill-news.png | News 新闻列表页 |
| puskill-help.png | Help 帮助中心页 |
| puskill-video.png | Video 视频页 |
| puskill-contact.png | Contact us 联系页 |
| puskill-product-detail.png | 产品详情页（DDR3样本） |

---

*报告结束*
