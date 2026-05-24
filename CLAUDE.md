# MyNotes Vault

本 Vault 遵循 Andrej Karpathy 的 LLM Wiki 方法论。

## 目录结构

```
MyNotes/
├── raw/                  # 原始素材（只读，不可变）
├── wiki/                 # LLM 编译的结构化知识
│   ├── index.md          # 内容索引（查询入口）
│   ├── log.md            # 操作日志（只追加）
│   ├── 项目/             # 项目笔记
│   ├── 技术问题/         # 故障排查笔记
│   └── 工具配置/         # 工具安装与配置笔记
└── CLAUDE.md             # 本规则文件
```

## LLM 操作约定

### Ingest（摄入）
- 用户放入 `raw/` 的素材由 LLM 阅读后编译到 `wiki/`
- 编译结果更新 `wiki/index.md` 索引
- 在 `wiki/log.md` 追加一条操作记录

### Query（查询）
- 先读 `wiki/index.md` 定位页面
- 回答时带回链引用

### Archive（回写）
- 有价值的查询答案写入 `wiki/` 成为持久知识

### Lint（健康检查）
- 检查断链、孤立页面、过时内容
- 发现矛盾时标注建议

## 同步规则
- `.obsidian/` 不上传（已 gitignore）
- 每次笔记变更后 commit + push 到 `Sober05/MyNotes`
