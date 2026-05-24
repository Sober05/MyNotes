# Karpathy LLM Wiki 方法论

Andrej Karpathy（OpenAI 联创、前 Tesla AI 总监）的个人知识管理系统。

---

## 三层架构

| 层 | 目录 | 角色 |
|----|------|------|
| Raw | `raw/` | 原始素材，只读不可变 |
| Wiki | `wiki/` | LLM 编译的结构化知识，持续维护 |
| Rules | `CLAUDE.md` | 定义结构、约定、工作流 |

## 四大操作

1. **Ingest（摄入）** — 新素材放入 raw/ → LLM 阅读 → 创建/更新 wiki 页面 → 更新索引
2. **Query（查询）** — 自然语言提问，LLM 从 `wiki/index.md` 定位，综合回答带回链
3. **Archive（回写）** — 好的查询答案归档回 wiki，知识库越用越聪明
4. **Lint（健康检查）** — 检查矛盾、过时、断链、孤立页面

## 核心文件

- `wiki/index.md` — 总索引，LLM 每次查询先读
- `wiki/log.md` — 操作日志，只追加不修改

## 核心哲学

- **Explicit** — 知识可见可导航，不在黑箱
- **Yours** — 数据在本地，不绑厂商
- **File over App** — 纯 Markdown，永久可读
- **BYOAI** — 想用哪个 AI 用哪个

> Karpathy 金句：「Obsidian 是 IDE，LLM 是程序员，Wiki 是代码库。」

---

> 2026-05-24 首次引入此方法论重组本 vault
