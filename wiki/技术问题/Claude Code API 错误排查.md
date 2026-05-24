# Claude Code API 错误排查

## 发现时间
2026-05-24

## 现象

连续多个会话出现网络错误：

| 状态码 | 错误类型 | 说明 |
|--------|----------|------|
| **524** | TencentEdgeOne 超时 | CDN/代理层等待上游 API 超时 |
| **500** | Internal Server Error | API 服务端内部错误 |
| HTTP 200 (空) | 代理截断 | 响应被中间网关截断，返回空/malformed 数据 |

## 排查过程

1. 读取 `.claude/projects/` 下的会话日志 JSONL 文件
2. 搜索 `api_error` 关键词定位故障记录
3. 发现多个 `subtype: api_error` 条目，含重试记录 (retryAttempt, maxRetries=10)

## 附带发现

**Stop Hook 脚本缺失：** 配置中引用 `python C:\Users\20159\.claude\chat-server\push_context.py`，但该文件不存在，导致每次会话结束报错。

## 结论

- **根因：** 服务端临时故障，非本地环境问题
- **Hook 缺失：** 文件已手动补全 (`C:\Users\20159\.claude\chat-server\push_context.py`)
- **恢复：** 后续会话正常

## 相关页面

- [[工具配置/Claude Code Skills 列表]] — 全部 Skills 参考
