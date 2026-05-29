# CC-Switch 使用指南

> 开源工具，统一管理 Claude Code / Codex / Gemini CLI 的 API 配置，免费。
> GitHub: [farion1231/cc-switch](https://github.com/farion1231/cc-switch) | 官网: [ccswitch.io](https://ccswitch.io)

## 安装

- Windows: 下载 `.msi` 双击安装。SmartScreen 弹警告 → 「更多信息」→「仍要运行」
- 如启动报错缺少 WebView2：装 [Microsoft Edge WebView2](https://developer.microsoft.com/en-us/microsoft-edge/webview2/)
- macOS: `brew install --cask cc-switch`

## 配置流程

### 1. 添加供应商
右上角 **+** → 「预设」下拉选供应商（DeepSeek / 智谱 / Kimi / MiniMax 等）→ 填 API Key → 「添加」

### 2. 配置模型
填模型名（如 `deepseek-v4-pro`），或点「自动获取模型」

### 3. 启用
主界面点供应商卡片的 **「启用」**

### 4. 验证
终端运行 `claude`，正常对话即配置成功

## 切换供应商

- **主界面**：点另一个供应商的「启用」
- **托盘**：右下角系统托盘右键 → 选供应商
- Claude Code 支持热重载，切换后即时生效

## 自定义配置

选「自定义」预设，手动填 JSON：

```json
{
  "env": {
    "ANTHROPIC_API_KEY": "你的API-Key",
    "ANTHROPIC_BASE_URL": "https://api.你的供应商.com",
    "ANTHROPIC_MODEL": "模型名",
    "ANTHROPIC_DEFAULT_SONNET_MODEL": "模型名",
    "ANTHROPIC_DEFAULT_OPUS_MODEL": "模型名",
    "ANTHROPIC_DEFAULT_HAIKU_MODEL": "模型名"
  }
}
```

## 实用开关

| 开关 | 作用 |
|------|------|
| 隐藏署名 | 提交/PR 不带 AI 署名 |
| 最大强度思考 | thinking effort 拉满 |
| 禁用自动更新 | 阻止 Claude Code 自动升级 |

## 常见问题

| 问题 | 解决 |
|------|------|
| 切换后不生效 | 检查 API Key 和 URL |
| 恢复官方 Anthropic | 选「Claude 官方」预设 |
| 环境变量冲突 | 清除系统中的 `ANTHROPIC_AUTH_TOKEN` 和 `ANTHROPIC_BASE_URL` |
