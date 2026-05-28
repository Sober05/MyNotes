# SitePro 企业官网模板

> 用 Next.js 搭建的中英文双语企业官网模板，猪八戒接单作品案例，快速改内容即可交付客户

## 技术栈

| 层 | 技术 |
|------|------|
| 框架 | Next.js 15 + React 19 |
| 语言 | TypeScript |
| 样式 | Tailwind CSS v4 |
| 国际化 | 手写 LanguageContext（不依赖第三方 i18n 库） |

## 功能清单

- 中英文双语切换（页面级，非路由跳转）
- 响应式布局（PC/手机/平板全适配）
- 7 个模块：导航 / Hero / 关于我们 / 服务项目 / 案例展示 / 联系表单 / 页脚
- 导航栏滚动自适应（透明→白色毛玻璃）
- 联系表单提交成功状态
- 案例卡片 hover 上浮动效
- 服务卡片 SVG 图标 + hover 效果
- Hero 暗色全屏 + 径向光晕 + 网格纹理
- About 左右双栏 + "在线接单中"浮动状态卡

## 文件位置

```
C:\Users\20159\corp-site-template\
  src/
    app/
      layout.tsx          # 根布局 + LanguageProvider 包裹
      page.tsx            # 首页：组合所有组件
      globals.css         # Tailwind 导入 + 基础样式
    components/
      Navbar.tsx          # 导航栏（透明/白色自适应）
      Hero.tsx            # 首屏全屏大图
      About.tsx           # 关于我们（双栏+数据+浮动卡）
      Services.tsx        # 服务项目（6格 SVG 图标）
      Cases.tsx           # 案例展示（3列+斜纹纹理）
      Contact.tsx         # 联系表单（暗色主题）
      Footer.tsx          # 页脚
    i18n/
      translations.ts     # 中英文词条
      LanguageContext.tsx # 语言切换 Context
```

## 启动方式

```bash
cd C:\Users\20159\corp-site-template
./node_modules/.bin/next dev
# 浏览器访问 http://localhost:3002
```

> npm 源已设置为 `https://registry.npmmirror.com`（淘宝镜像）

## 排错记录

| 问题 | 解决 |
|------|------|
| Next.js 16.2.6 Windows SWC WASM `invalid type: unit value` 报错 | 降级到 Next.js 15.5.18 |
| Turbopack 不支持 Windows x64 | Next.js 15 默认用 Webpack，无需特别处理 |
| `npx next` 找不到命令（`.bin/` 为空） | Windows npm symlink 问题，用 `./node_modules/.bin/next` 完整路径 |
| npm 安装极慢 | 切换到淘宝镜像 `registry.npmmirror.com` |
| Footer 组件 500 错误 | 遗漏 `'use client'` 指令，useLang() 是客户端 hook |

## 猪八戒接单使用方式

1. 接到客户需求 → 改 `translations.ts` 里对应文案 → 截图发客户确认
2. 改 `components/` 里的颜色、内容、案例名
3. `npm run build` 导出静态文件 → 部署到客户服务器
