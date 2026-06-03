# SitePro 企业官网模板

> Next.js 中英文双语企业官网。历经 impeccable + taste-skill + ui-ux-pro-max 三轮设计打磨 + 专业审计修复。

## 技术栈

| 层 | 技术 |
|------|------|
| 框架 | Next.js 15 + React 19 |
| 语言 | TypeScript |
| 样式 | Tailwind CSS v4 |
| 国际化 | 手写 LanguageContext（不依赖第三方 i18n 库） |
| 动画 | 手写 useReveal hook（IntersectionObserver + 淡入） |

## 页面结构（8 个模块）

```
Hero       ██ 深色全屏摄影 + 品牌标语 + 白色CTA
About      ░░ 左栏数字+照片 / 右栏斜体引子+文字+细线列表
Services   ░░ 浅灰底 + 大标题直入 + 细线分隔6格网格(编号01-06)
Cases      ░░ 三行列表 + hover缩略图露出 + 箭头链接
Trusted    ░░ 浅灰底 + 三栏客户评价 + 头字母头像 + 公司名
Contact    ██ 深色全宽 + 下划线表单 + 信任信号(头像+200+客户)
Footer     ██ 深色
```

## 组件清单

```
src/
  app/
    layout.tsx          # 根布局 + LanguageProvider
    page.tsx            # 首页：组合8个组件
    globals.css         # Tailwind 导入
  components/
    Navbar.tsx          # 导航栏 + 汉堡菜单(移动端) + 跳过链接(a11y)
    Hero.tsx            # 全屏摄影背景 + 品牌标语
    About.tsx           # 左右双栏 + 统计数字 + 斜体引子
    Services.tsx        # 6格细线网格 + 编号(01-06)
    Cases.tsx           # 3行列表 + hover缩略图 + 文字链接
    Trusted.tsx         # 3栏客户评价(新增)
    Contact.tsx         # 深色表单 + 下划线输入框
    Footer.tsx          # 深色Logo + 版权
  hooks/
    useReveal.ts        # 滚动触发淡入动画(新增)
  i18n/
    translations.ts     # 中英文词条
    LanguageContext.tsx  # 语言切换Context
```

## 启动方式

```bash
cd C:\Users\20159\corp-site-template
./node_modules/.bin/next dev
# 浏览器访问 http://localhost:3000
```

> npm 源已设置为 `https://registry.npmmirror.com`（淘宝镜像）

## 设计审计修复记录

| 优先级 | 问题 | 修复 |
|------|------|------|
| P0 | 移动端导航缺失 | 汉堡菜单 + 展开动画 + 三线变X微交互 |
| P0 | Cases 图片数组未使用 | 转为hover缩略图 + 文字链接替代箭头圆圈 |
| P1 | 5个Section标签+标题模式雷同 | About用斜体引子、Services去标签、Contact换行动导向标题 |
| P1 | 品牌无个性 + 无社会证明 | Hero品牌标语("不套模板，不流水线")、新增Trusted组件(3条客户评价)、Contact加头像信任信号 |
| P2 | 色彩摇摆 + 无动画 + 对比度 | 暗-浅-浅灰-浅-浅灰-暗节奏、useReveal滚动淡入(4个Section)、Services文字对比度修正 |

## 排错记录

| 问题 | 解决 |
|------|------|
| Next.js 16.2.6 Windows SWC WASM `invalid type: unit value` 报错 | 降级到 Next.js 15.5.18 |
| Turbopack 不支持 Windows x64 | Next.js 15 默认用 Webpack |
| `npx next` 找不到命令（`.bin/` 为空） | Windows npm symlink 问题，用 `./node_modules/.bin/next` |
| npm 安装极慢 | 切换到淘宝镜像 |
| Footer 组件 500 错误 | 遗漏 `'use client'` 指令 |
