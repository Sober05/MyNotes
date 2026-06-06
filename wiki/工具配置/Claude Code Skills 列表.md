# Claude Code Skills 列表

Skills 是 Claude Code 的子能力模块，通过 `/skill名` 或对话触发词自动激活。

> 最后更新：2026-06-07 | 共 132 个 skills

---

## 📰 资讯类

### aihot
- **功能：** 中文 AI 资讯查询，拉取 AI HOT 公开 API 数据并整理为中文简报
- **触发：** "今天 AI 圈有什么"、"AI 日报"、"AI 资讯"、"最近 AI"、"OpenAI/Anthropic/Google 最近发布了什么"、"看一下 AI 行业动态"、"AI HOT 精选"等
- **无需配置** API Key

## 📝 写作类

### khazix-writer
- **功能：** 公众号长文写作（数字生命卡兹克风格）
- **触发：** "写文章"、"写稿子"、"帮我写"、"续写"、"扩写"、"公众号文章"、"出稿"、"按我的风格写"
- **支持素材：** PDF、brief、新闻链接、语音转文字
- **不适用：** 短内容（小红书/推特/朋友圈）、纯标题

### chinese-thesis-workbench 📌 新增
- **功能：** 本科毕业论文标准化交付工作台 — 材料摄入→证据提取→文献治理→分章写作→DOCX 成稿→质量检查
- **触发：** "写论文"、"毕业论文"、"本科论文"、"开题报告"、"文献综述"、"生成docx"、"AIGC降重"、"论文格式"
- **交付路径：** M1 默认样式 / M2 样文贴进 / M3 模板填充（推荐） / M4 已有稿编辑
- **依赖：** Python (pypdf / python-docx / PyYAML) + Node/Playwright（可选，自动截图用）
- **来源：** github.com/ZyhSechub/chinese-thesis-workbench-skill (392+ stars)

### internal-comms
- **功能：** 内部通讯写作（状态报告、领导层更新、公司通讯、FAQ、事故报告等）
- **触发：** 需要写内部通讯文档时

## 🔬 研究分析类

### hv-analysis
- **功能：** 横纵分析法深度研究（历时-共时双轴分析），产出 PDF 研究报告
- **触发：** "研究一下"、"帮我分析"、"深度研究"、"做个研究"、"竞品分析"、"帮我看看这个东西怎么样"、"帮我摸清楚"、"deep research"
- **不适用：** 简单名词解释、公众号写作、纯标题摘要

## 🛠️ 开发工具类

### mcp-builder
- **功能：** 创建 MCP (Model Context Protocol) 服务器，让 LLM 与外部服务交互
- **技术栈：** Python (FastMCP) / Node/TypeScript (MCP SDK)

### mcp-integration
- **功能：** 将 MCP 服务器集成到 Claude Code 插件中
- **触发：** "add MCP server"、"integrate MCP"、"configure MCP"、"set up Model Context Protocol"

### claude-api
- **功能：** 构建、调试和优化 Claude API / Anthropic SDK 应用（含 prompt caching）
- **触发：** 代码中导入 `anthropic` / `@anthropic-ai/sdk`
- **不适用：** OpenAI SDK、其他 LLM 提供商

### find-skills
- **功能：** 发现和安装 agent skills（Skills 生态搜索引擎）
- **触发：** "how do I do X"、"find a skill for X"、"is there a skill that can..."
- **来源：** vercel-labs/skills

### skill-creator
- **功能：** 创建、修改和优化 skills，运行 evals 测试 skill 性能
- **触发：** "create a skill"、"edit a skill"、"optimize a skill"

### webapp-testing
- **功能：** 使用 Playwright 测试本地 web 应用（截图、调试 UI、查看浏览器日志）
- **触发：** 需要测试前端功能、调试 UI 行为时

### browser-testing-with-devtools
- **功能：** 通过 Chrome DevTools MCP 在真实浏览器中测试
- **触发：** 构建/调试浏览器运行的应用、检查 DOM、捕获控制台错误、分析网络请求
- **需要：** chrome-devtools MCP server

### deploy-to-vercel
- **功能：** 部署应用到 Vercel
- **触发：** "deploy my app"、"deploy and give me the link"、"push this live"、"create a preview deployment"

### vercel-cli-with-tokens
- **功能：** 使用 token 认证的 Vercel CLI 部署和管理项目
- **触发：** "deploy to vercel"、"set up vercel"、"add environment variables to vercel"

### run
- **功能：** 启动并驱动项目应用，确认更改生效

### template-skill
- **功能：** Skills 模板，用于创建新 skill 时的参考

## 🎨 前端开发类

### frontend-design
- **功能：** 创建有设计品质的生产级前端界面，告别"AI 廉价感"
- **触发：** "build a landing page"、"create a dashboard"、"design a website"、React 组件、HTML/CSS 布局
- **来源：** anthropics/skills

### frontend-ui-engineering
- **功能：** 构建生产级 UI，管理组件、布局、状态
- **触发：** 构建/修改用户界面，需要生产级外观时

### vercel-react-best-practices
- **功能：** Vercel 工程团队的 React/Next.js 性能优化指南（69 条规则）
- **触发：** 编写/审查 React 组件、Next.js 页面、数据获取、打包优化

### vercel-composition-patterns
- **功能：** React 组合模式（compound components、render props、context providers）
- **触发：** 重构 boolean prop 泛滥的组件、构建灵活组件库
- **包含：** React 19 API 变更

### vercel-react-native-skills
- **功能：** React Native 和 Expo 移动端最佳实践
- **触发：** 构建 RN 组件、优化列表性能、实现动画

### vercel-react-view-transitions
- **功能：** React View Transition API 动画（页面过渡、路由动画、共享元素动画）
- **触发：** 添加页面过渡、动画路由变化、Next.js 视图过渡

### vercel-optimize
- **功能：** Vercel 成本和性能优化（Next.js、SvelteKit、Nuxt 等）
- **触发：** Vercel 账单降低、慢路由、缓存优化、Core Web Vitals

### web-design-guidelines
- **功能：** Web 界面指南合规审查（无障碍、UX、最佳实践）
- **触发：** "review my UI"、"check accessibility"、"audit design"、"review UX"

### web-artifacts-builder
- **功能：** 构建复杂 claude.ai HTML artifacts（React、Tailwind CSS、shadcn/ui）
- **触发：** 需要状态管理、路由或 shadcn/ui 的复杂 artifact

### theme-factory
- **功能：** 为 artifacts 应用主题样式（10 种预设 + 自定义）
- **触发：** 为 slides、docs、HTML 页面应用主题

### brand-guidelines
- **功能：** 应用 Anthropic 品牌颜色和排版
- **触发：** 需要 Anthropic 品牌风格时

### canvas-design
- **功能：** 创建视觉艺术设计（.png / .pdf 海报、设计、静态作品）
- **触发：** "create a poster"、"piece of art"、"design"

### algorithmic-art
- **功能：** 使用 p5.js 创建算法艺术（流场、粒子系统等）
- **触发：** "generative art"、"algorithmic art"、"flow fields"

### impeccable
- **功能：** 前端设计审计与打磨（AI slop检测、启发式评分、可访问性、反模式、品牌/产品双注册）
- **触发：** "design"、"redesign"、"critique"、"audit"、"polish"、"improve a frontend interface"
- **命令：** craft, shape, critique, audit, polish, bolder, quieter, distill, harden, animate, colorize, typeset, layout, delight, overdrive, clarify, adapt, optimize, live, teach, document, extract
- **来源：** pbakaus/impeccable (53.5K installs)

### taste-skill
- **功能：** 高主动性前端品味技能，可调设计差异度、动效强度、视觉密度，阻止通用 UI 廉价感
- **触发：** 前端设计需要品味判断、差异化、动效或密度调整时
- **来源：** nexu-io/open-design@taste-skill (439 installs)

### ui-ux-pro-max
- **功能：** UI/UX 设计智能引擎：57种UI样式、95套调色板、56组字体配对、99条UX指南、25种图表、10个技术栈。含 Python CLI 搜索引擎
- **触发：** UI/UX 设计、构建、审查、修复、改进、优化、增强、重构
- **来源：** nextlevelbuilder/ui-ux-pro-max-skill (12.7K stars)
- **配套：** ckm-ui-styling / ckm-design-system / ckm-design / ckm-brand / ckm-banner-design / ckm-slides（共7个 skills）

### building-native-ui
- **功能：** Expo Router + React Native 原生 UI 构建完整指南：导航、动画、原生标签、表单、媒体、图标、搜索、存储等
- **触发：** Expo/React Native UI 开发
- **来源：** expo/skills (702 stars)
- **配套：** expo-api-routes / expo-dev-client / expo-deployment / expo-tailwind-setup / expo-ui-swiftui / expo-ui-jetpack-compose / native-data-fetching / upgrading-expo / use-dom 等（共16个 skills）

### grill-me
- **功能：** 写代码前反复盘问你的计划，遍历设计树的每个分支逐项解决依赖决策，直到完全理解需求
- **触发：** `/grill-me` + 想法
- **来源：** mattpocock/skills (77K+ stars)

### grill-with-docs
- **功能：** 结合文档深度审查代码

### diagnose / triage / qa
- **功能：** 诊断问题根因 / 问题分诊优先级排序 / 质量保证审查
- **来源：** mattpocock/skills

### tdd
- **功能：** 测试驱动开发，先写测试再写代码
- **来源：** mattpocock/skills

### prototype / design-an-interface
- **功能：** 快速原型构建 / 界面设计
- **来源：** mattpocock/skills

### caveman / handoff / write-a-skill
- **功能：** 用最简单的话解释复杂概念 / 项目交接文档 / 教你写自定义 Skill
- **来源：** mattpocock/skills

### amap
- **功能：** 高德 Web Service API 脚本：地理编码、逆地理编码、IP定位、天气、路径规划、距离测量、POI查询
- **触发：** "高德/AMap 查询"、"路线规划"、"地理编码"、"POI 搜索"
- **来源：** kaichen/amap-skill (421 installs)

## 📊 演示与文档类

### ppt
- **功能：** 创建 PowerPoint 演示文稿
- **触发：** "做个 PPT"、"PowerPoint"、"presentation"、"slides"

### pptx
- **功能：** .pptx 文件的创建、读取、编辑、合并、拆分
- **触发：** 任何涉及 .pptx 文件的操作

### docx
- **功能：** Word 文档 (.docx) 的创建、读取、编辑、操作
- **触发：** "Word doc"、".docx"、生成报告/备忘录/信函/模板

### pdf
- **功能：** PDF 文件的读取、合并、拆分、旋转、水印、加密、OCR
- **触发：** 任何涉及 .pdf 文件的操作

### xlsx
- **功能：** 电子表格 (.xlsx/.csv/.tsv) 的创建、读取、编辑、图表
- **触发：** 任何涉及电子表格文件的操作

### doc-coauthoring
- **功能：** 结构化文档协作写作工作流
- **触发：** "write documentation"、"create a proposal"、"draft a spec"

### documentation-and-adrs
- **功能：** 记录架构决策和文档
- **触发：** 做架构决策、变更公共 API、发布功能

### slack-gif-creator
- **功能：** 创建优化用于 Slack 的动画 GIF
- **触发：** "make me a GIF of X doing Y for Slack"

## ✅ 代码质量类

### code-review
- **功能：** 代码审查，检查 diff 中的 bug
- **强度：** low/medium（高置信度）/ high→max（广覆盖）

### security-review
- **功能：** 对当前分支的待定更改进行安全审查

### verify
- **功能：** 通过运行应用并观察行为来验证代码更改

### systematic-debugging
- **功能：** 系统化根因调试，遇到任何 bug/测试失败/异常行为时使用
- **触发：** 测试失败、构建中断、行为不符合预期

### test-driven-development
- **功能：** 测试驱动开发，在实现前先写测试
- **触发：** 实现任何逻辑、修 bug、变更行为
- **来源：** obra/superpowers + addyosmani/agent-skills（双版本）

### verification-before-completion
- **功能：** 声称完成/修复/通过前强制运行验证
- **触发：** commit 或创建 PR 之前

### requesting-code-review
- **功能：** 完成重要功能或合并前请求代码审查

### receiving-code-review
- **功能：** 收到代码审查反馈后，验证后再实施（不盲目接受）

### code-review-and-quality
- **功能：** 多轴代码审查（合并前全面质量评估）

### code-simplification
- **功能：** 简化代码提高可读性（不改行为）
- **触发：** 重构以提高清晰度

### security-and-hardening
- **功能：** 安全加固（防止命令注入、XSS、eval 等）
- **触发：** 处理用户输入、认证、数据存储、外部集成

### debugging-and-error-recovery
- **功能：** 系统化调试和错误恢复指南

### doubt-driven-development
- **功能：** 对每个非平凡决策进行新鲜上下文对抗审查
- **触发：** 正确性比速度重要、不熟悉的代码、高风险场景

## 🏗️ 软件工程实践类

### spec-driven-development
- **功能：** 在编码前创建 spec
- **触发：** 启动新项目/功能、需求不清晰时

### source-driven-development
- **功能：** 每个实现决策都以官方文档为支撑
- **触发：** 使用需要正确性的框架/库时

### api-and-interface-design
- **功能：** 稳定 API 和接口设计指南
- **触发：** 设计 REST/GraphQL 端点、定义模块间类型契约

### git-workflow-and-versioning
- **功能：** 结构化 git 工作流（commit、分支、冲突解决）

### ci-cd-and-automation
- **功能：** CI/CD 管线自动化
- **触发：** 设置/修改构建和部署管线

### performance-optimization
- **功能：** 应用性能优化（Core Web Vitals、加载时间、瓶颈修复）

### deprecation-and-migration
- **功能：** 废弃和迁移管理
- **触发：** 移除旧系统/API、用户迁移

### shipping-and-launch
- **功能：** 生产发布准备（上线检查清单、监控、分阶段发布、回滚策略）

### context-engineering
- **功能：** 优化 agent 上下文设置
- **触发：** 开启新会话、输出质量下降、切换任务

### incremental-implementation
- **功能：** 增量交付变更（一次一个文件，避免一次性大量代码）

### interview-me
- **功能：** 通过一问一答式访谈提取用户真实需求（达到 ~95% 置信度）
- **触发：** 需求模糊（"build me X" 没说清楚）、用户明确调用

### idea-refine
- **功能：** 通过结构化发散-收敛思维将原始想法精炼为可操作概念
- **触发：** "ideate"、"refine this idea"、"stress-test my plan"

## 🏗️ 项目管理类

### init
- **功能：** 初始化新的 CLAUDE.md 文件

### neat-freak
- **功能：** 会话结束后清理和同步项目文档与记忆
- **触发：** "sync up"、"tidy up docs"、"整理文档"、"梳理一下"、"收尾"

### sync-obsidian
- **功能：** 会话结束后自动将对话摘要同步到 Obsidian Vault 并推送 GitHub
- **触发：** "保存对话"、"同步到obsidian"、"写入obsidian"、"存档"、"记下来"、"写进obsidian"、"/sync-obsidian"
- **Vault 路径：** `C:\Users\20159\OneDrive\Desktop\笔记\MyNotes\`
- **GitHub：** `Sober05/MyNotes`

### review
- **功能：** 审查 Pull Request

### brainstorming
- **功能：** 任何创意工作前探索用户意图、需求和设计
- **触发：** 创建功能、构建组件、添加功能、修改行为之前（必须使用）

### writing-plans
- **功能：** 多步骤任务前写实现计划

### executing-plans
- **功能：** 在独立会话中执行已写的实现计划（含审查检查点）

### subagent-driven-development
- **功能：** 在当前会话中执行含独立任务的实现计划

### dispatching-parallel-agents
- **功能：** 处理 2 个以上无共享状态/顺序依赖的独立任务

### planning-and-task-breakdown
- **功能：** 将工作分解为有序任务
- **触发：** 有 spec 需要分解、任务太大无法开始、需要估算范围

### finishing-a-development-branch
- **功能：** 完成开发分支的收尾（merge、PR 或清理选项）

### using-superpowers
- **功能：** 启动任何对话时建立 skills 使用流程（必须使用）

### using-agent-skills
- **功能：** 发现和调用 agent skills 的元 skill

### using-git-worktrees
- **功能：** 为特性工作创建隔离的 git worktree

## 🚀 产品与创业类

### theminimailistentrepreneur
- **功能：** 极简创业者方法论产品顾问，用社区先行、第一天收费、精益不融资等原则指导小程序/产品决策
- **触发：** "小程序"、"产品设计"、"功能决策"、"定价"、"增长"、"赚钱"、"要不要做某个功能"、"项目方向"、"创业想法"、"副业项目"、"独立开发"
- **基于：** Sahil Lavingia《The Minimalist Entrepreneur》+ 小程序变现实战经验

## ⚙️ 配置类

### update-config
- **功能：** 配置 settings.json（权限、env 变量、hooks 等）
- **触发：** "allow X"、"添加权限"、"设置环境变量"、hook 故障排查

### keybindings-help
- **功能：** 自定义键盘快捷键
- **触发：** "rebind ctrl+s"、"add a chord shortcut"、"自定义快捷键"

### fewer-permission-prompts
- **功能：** 扫描对话记录中的常用只读 Bash/MCP 调用，添加白名单减少权限提示

## 🔁 自动化类

### loop
- **功能：** 按固定间隔重复运行一个 prompt 或 slash command
- **用法：** `/loop 5m /foo`，默认间隔 10 分钟

---
> 最后更新：2026-06-07 | 共 132 个 skills
