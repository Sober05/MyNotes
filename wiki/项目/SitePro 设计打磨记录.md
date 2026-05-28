# SitePro 设计打磨记录

> 三轮设计 Skill 打磨 + 一次专业审计 + 逐项修复的完整记录

## 第一轮：impeccable（反 AI slop 审计）

**违反的法则：**

| 法则 | 位置 | 修复 |
|------|------|------|
| 渐变文字（绝对禁止） | Hero h1 第二行 `bg-clip-text text-transparent` | 改为纯色 `text-blue-600` |
| Hero 指标模板（绝对禁止） | Hero 底部 3 个数字+标签 | 替换为 Unsplash 办公场景照片 |
| 相同卡片网格（绝对禁止） | Services 6 张 icon+标题+描述 | 改为非对称网格(2/3 + 1/3) |
| 重复大写标签（品牌禁令） | 每个 Section 的 `tracking-widest uppercase` | 移除所有 |
| 零图片（品牌禁令） | 全站无真实图片 | Hero/About/Cases 各加 Unsplash 照片 |
| 导航栏玻璃态默认 | `backdrop-blur` | 改为纯白背景 + shadow |
| 标签不关联输入框 | Contact 表单 `<label>` + `<input>` | 添加 `htmlFor` + `id` |
| 触摸目标 < 44px | 语言切换按钮 | `py-2 min-h-[44px]` |
| 无跳过链接 | Navbar | 添加 `sr-only` 跳过导航 |

## 第二轮：taste-skill（品味升级）

| 维度 | 改动 |
|------|------|
| Hero | 全屏深色毛玻璃 + 实景摄影 + 左侧竖线装饰 + 白色实心CTA |
| 色彩 | 饱和度克制，蓝色仅用于Logo+标题第二行 |
| Services | 细线分隔密集网格（`gap-px`）+ 编号 `01-06` 代替 SVG 图标 |
| Cases | 极简行列表：编号 + 标题/行业 + 描述 + hover 箭头 |
| About | 左栏数字+照片 / 右栏文字+细线列表，不对称比例 5:7 |
| Contact | 深色全宽 + 下划线输入框 + 箭头提交按钮 |
| 细节 | 无渐变、纯色过渡、`rounded-md` 统一圆角 |

## 第三轮：ui-ux-pro-max（专业收尾）

| 规则 | 修复 |
|------|------|
| 文字对比度 | 三个亮色 section 正文 `text-gray-500` → `text-gray-600` |
| cursor-pointer | Services 卡片 + Cases 行 + 所有可交互元素 |
| 过渡时长统一 | Navbar `duration-500→300`、Cases 补 `duration-200`、Contact 输入框补 `duration-200` |
| 统计标签 | About 统计标签 `text-gray-400→500` |

## 第四轮：专业设计审计 + 逐项修复

发现 11 个问题（P0×2 + P1×3 + P2×3 + P3×3），全部修复：

| # | 优先级 | 问题 | 修复 |
|------|------|------|------|
| 1 | P0 | 移动端导航缺失 | 汉堡菜单 + 展开动画 + 三线变X |
| 2 | P0 | Cases 图片数组未使用 | hover缩略图 + 文字链接 |
| 3 | P1 | 标签+标题模式雷同 | 3种不同Section头部风格 |
| 4 | P1 | 品牌无个性 | Hero 品牌标语 + Trusted 评价组件 |
| 5 | P1 | 无社会证明 | 3条客户评价 + 头像 + 公司名 |
| 6 | P2 | 色彩摇摆 | 统一暗-浅-浅灰-浅-浅灰-暗节奏 |
| 7 | P2 | 无入场动画 | useReveal hook(IntersectionObserver) |
| 8 | P2 | Services对比度 | text-gray-600 |
