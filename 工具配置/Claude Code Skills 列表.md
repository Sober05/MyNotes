# Claude Code Skills 列表

Skills 是 Claude Code 的子能力模块，通过 `/skill名` 或对话触发词自动激活。

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
- **覆盖：** SSE、stdio、HTTP、WebSocket 等 MCP 类型

### claude-api
- **功能：** 构建、调试和优化 Claude API / Anthropic SDK 应用（含 prompt caching）
- **触发：** 代码中导入 `anthropic` / `@anthropic-ai/sdk`；调整 caching/thinking/tool use/batch/files/citations/memory 等功能
- **不适用：** OpenAI SDK、其他 LLM 提供商

## 📊 演示与文档类

### ppt
- **功能：** 创建 PowerPoint 演示文稿
- **触发：** "做个 PPT"、"PowerPoint"、"presentation"、"slides"

## ✅ 代码质量类

### code-review
- **功能：** 代码审查，检查 diff 中的 bug
- **强度：** low/medium（高置信度）/ high→max（广覆盖，可能含不确定项）
- **用法：** 可选 `--comment` 将发现作为 PR 内联评论发布

### security-review
- **功能：** 对当前分支的待定更改进行安全审查

### verify
- **功能：** 通过运行应用并观察行为来验证代码更改
- **触发：** "验证 PR"、"确认修复"、"测试更改"、"检查功能"、"验证本地更改"

## 🏗️ 项目管理类

### init
- **功能：** 初始化新的 CLAUDE.md 文件，用于项目文档

### neat-freak
- **功能：** 会话结束后清理和同步项目文档与记忆
- **触发：** "sync up"、"tidy up docs"、"整理文档"、"更新记忆"、"同步一下"、"梳理一下"、"收尾"、"这个阶段做完了"

### review
- **功能：** 审查 Pull Request

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
- **用法：** `/loop 5m /foo`
- **默认间隔：** 10 分钟

### run
- **功能：** 启动并驱动项目应用，确认更改生效
- **不限于：** CLI、server、TUI、Electron、浏览器驱动、library 类项目

---

> 最后更新：2026-05-24
