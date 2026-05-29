# 操作日志

> 只追加，不修改。记录 wiki 的所有变更。

---

- **2026-05-24 17:42** — 新增学习模块：护理学期末 5 周突击计划（内科/外科/儿科/急危重症），含逐日排期+考点拆解+题型分析+错题库
- **2026-05-24 17:15** — **Lint 检查**：修复 1 处过时内容（Git-GitHub 状态），添加 4 个交叉引用（Obsidian↔Karpathy↔GitHub, API排查↔Skills）
- **2026-05-24 17:10** — 按 Karpathy LLM Wiki 方法论重组 vault：创建 `raw/` `wiki/`，迁移所有笔记到 `wiki/`，建立 `CLAUDE.md` 规则文件
- **2026-05-24 17:04** — 添加 Claude Code Skills 列表，收录 16 个 Skills
- **2026-05-26 14:35** — 桌面文件大整理：按功能分类为 8 个中文文件夹（项目/技能插件/文档资料/图片素材/快捷方式/笔记/软件工具/其他），MyNotes vault 迁移至 `笔记/MyNotes/`
- **2026-05-26 15:00** — 开发桌面宠物应用：PyQt5 像素猫，DeepSeek API 驱动，支持聊天对话、文件拖拽分析、系统托盘、空闲检测自动睡觉、心情系统、定时提醒、剪贴板监控、快速启动菜单
- **2026-05-26 15:30** — 桌面宠物全面中文化 + 修复 HTML 注入崩溃 + 修复流式输出线程安全问题
- **2026-05-26 14:20** — 配置 Claude Code Statusline（上下文用量可视化进度条，Python 脚本，5s 刷新）
- **2026-05-26 18:50** — 桌面宠物稳定性升级：单实例锁、崩溃看门狗、API 15s 超时、启动健康检查、错误日志系统
- **2026-05-26 18:55** — 代码重构：拆分 pet_window.py（150行）+ pet_systems.py（250行），聊天历史持久化（chat-history.json）
- **2026-05-26 19:00** — 对话框优化：新增 X 关闭按钮 + Esc 关闭 + 点击外部关闭（应用级事件过滤器）
- **2026-05-26 19:15** — 桌面宠物 v1.0 开源发布：修复安全隐私（env var 优先、gitignore）、去硬编码、跨平台空闲检测、统一配置管理、MIT License → GitHub: Sober05/desktop-pet
- **2026-05-26 19:40** — 桌宠 v1.0.1 优化：心情表情系统（3种）、右键菜单补全（设置开关+关于）、对话框智能定位（不遮挡宠物）、Esc/点击外部稳定关闭、防误触阈值提升
- **2026-05-26 19:45** — 修复启动崩溃（PetSystems 初始化顺序）+ 快捷方式改用 pythonw 无窗口启动
- **2026-05-26 19:20** — 创建 sync-obsidian Skill：对话自动同步 Obsidian + GitHub
- **2026-05-28 全天** — 自由职业启动日：研究猪八戒平台行情与定价、盘点本地技术栈（Node.js/Python/微信开发者工具）、确定纯前端+企业官网方向、设计三档套餐（¥599/¥1999/¥4999）、搭建 SitePro 企业官网模板（Next.js 15 + Tailwind CSS + 中英文双语 + 响应式+7 模块）、经历 Next.js 16→15 降级/Windows SWC WASM 兼容/npm 淘宝镜像/Footer 'use client' 修复等排错、二轮设计升级（暗色 Hero/渐变/动画/SVG 图标/浮动卡片）
- **2026-05-28 下午** — 安装 4 个新 Skill：impeccable（设计审计/反AI痕迹）、taste-skill（品味判断/设计差异化）、ui-ux-pro-max（UI/UX专业打磨）、amap（高德地图API）
- **2026-05-28 下午** — SitePro 三轮设计打磨：(1) impeccable 审计修复5+处AI slop（渐变文字、hero指标模板、相同卡片网格、重复大写标签、零图片）、(2) taste-skill 品味升级（暗色摄影Hero、Services细线网格+编号、Cases极简行列表、Contact下划线表单）、(3) ui-ux-pro-max 专业收尾（文字对比度合规、cursor-pointer统一、transition时长归一）
- **2026-05-28 晚上** — 专业设计审计：发现11个问题（P0-P3），涉及移动端导航缺失、品牌无个性、标签模式滥用、无社会证明、无入场动画等。全部逐一修复：添加汉堡菜单+滚动动画hook(useReveal)+客户评价组件(Trusted)+品牌标语+Section头部多样化
- **2026-05-28 深夜** — 开发动漫混剪自动化流水线 (anime-pipeline)：Python CLI 工具，MoviePy + librosa + OpenCV，支持片段分析(动作分数/情绪分数/场景检测)、BGM 匹配(beat检测)、燃向/情绪向双模板编辑、自动标题标签生成、B站/抖音发布。鬼灭之刃无限列车 144 个片段已全部分析缓存
- **2026-05-28 深夜** — 修复 MoviePy 2.x API 兼容性：subclip→subclipped、volumex→with_volume_scaled、set_audio→with_audio、fx→with_effects、fl→with_updated_frame_function 等，涉及 editor.py/ran.py/qingxu.py 三个文件
- **2026-05-28 深夜** — 修复 Windows 页文件耗尽 (WinError 1455)：编辑器添加最大片段数限制(12)、最小文件大小过滤(500KB)、最小时长过滤(0.3s)，解决同时加载大量 ffmpeg 进程导致虚拟内存不足
- **2026-05-28 深夜** — 首次渲染成功: anime_ran.mp4 (25MB/22s/燃向)，但用户反馈自动生成质量差，后续改为提供人工剪辑建议
- **2026-05-28 深夜** — 为鬼灭之刃无限列车素材提供炎柱人物志剪辑方案：五段式结构(登场→战斗→台词→陨落→余韵)、BGM 建议、卡点与过渡技巧
- **2026-05-28 深夜** — 开发色感挑战小程序 v2：新增颜色匹配+颜色记忆双模式（从 2 模式扩展到 4 模式）、创建设计令牌系统（40+ CSS 变量内联到 app.wxss）、15+ 关键帧动画库、玻璃态 UI 重设计、震动反馈(haptics.ts)、音效系统(audio.ts 手写 WAV 生成+base64编码)、连击系统(Combo 弹出特效+分数乘数)、粒子爆发组件、结果页分数滚动动画+段位进度条、排行页骨架屏+空状态+错误重试
- **2026-05-28 深夜** — 色感挑战社交裂变：好友挑战系统（createChallenge/getChallenge 云函数 + challenge 页面 + VS 对战）、新手引导组件（tutorial-overlay 每模式 3 步遮罩）
- **2026-05-29 凌晨** — 色感挑战调试：(1) 僵尸 .js 脚手架文件删除让 TS 重新编译、(2) `IAppOption` 未 export 导致编译失败、(3) `btoa()` 不存在→手写 base64→`wx.arrayBufferToBase64` 不在类型定义→再改手写、(4) WXSS `@import` 路径解析不一致→全部内联、(5) 全局 300ms `_tapGuard` 导致色块→槽位连续点击被拦截→移除、(6) tutorial-overlay `visible` 默认 false 导致既看不到引导也进不了游戏→attached 时自动设为 true、(7) 最终回退到最小可用版本定位问题
- **2026-05-28 深夜** — clawd 桌宠安全审计（小龙虾多智能体审查）：发现 11 个问题，含 API Key 明文存储(严重)、剪贴板设置不生效(高)、截图积累(高)等。全部修复：清空 config.json 中的 Key 改用 DEEPSEEK_API_KEY 环境变量、修复 _toggle_clipboard 空函数、shared/ 退出自动清理
- **2026-05-28 深夜** — 桌宠启动失败排查：.pet-lock 残留 PID 被 Windows 复用导致单实例检测误判，将文件锁替换为 Windows 命名互斥体(CreateMutexW)彻底解决
- **2026-05-29 下午** — 色感挑战第三轮优化：(1) 修复 doubleBonus 提交 bug（服务端拒绝 mode:doubleBonus+单 round）、(2) 修复 checkAchievements spotPerfectStreak 连续计数bug、(3) 消除 submitScore 与 utils/score.ts 评分逻辑重复、(4) audio.ts 添加4个 InnerAudioContext 对象池、(5) game.ts 所有 tap handler + startRound try-catch 错误边界、(6) result 页新增本局统计（正确率/平均用时/最佳单轮）
- **2026-05-29 下午** — 色感挑战敏感信息脱敏：AppID 从 project.config.json 移到 project.private.config.json，云环境 ID 从 app.ts 抽离到 miniprogram/config.js。两者均加入 .gitignore，提供 config.example.js 模板。app.ts 改为 require('./config') 动态加载。
- **2026-05-29 下午** — 色感挑战源码打包为 GitHub Gist（5500行聚合文件，排除敏感配置），分享给 DeepSeek 审查
- **2026-05-29 下午** — 色感挑战第四轮深度审查（20项缺陷 P0-P3）：(P0) 5个云函数+1个前端 UTC→北京时间修复 (beijingDate函数)、(P1) particle-burst定时器泄漏修复、game.ts复活防重入锁、颜色生成deltaE下限 3→10+搜索算法加强、share-card Canvas 高DPR风险记录、(P2-P3) 排行榜缺昵称、新手引导无跳过选项、成就冷启动超时、广告占位符等。新增 runSelfCheck() 全局健康检查函数（14项自检）。审查报告上传为 GitHub Gist。
- **2026-05-29 下午** — sync-obsidian 同步本次会话全部变更
- **2026-05-29 19:45** — 色感挑战第五轮修复：(1) tsconfig/launch.json 微信开发者工具报错修复（JSON 注释移除、module→ES2020、types 移除、moduleResolution 添加）、(2) game.ts safeTap 后缺少逗号导致真机调试 SyntaxError、(3) 色相排序：移除自动提交 → 添加"确认提交"按钮 + 支持色块重新排列（点击已填入槽位移回源区 + 源区-槽位交换）、(4) 找不同色：答错 → 震动+红色描边+600ms 自动重置（冻结引擎防双击）、(5) 颜色匹配：答错 → 展示答案+800ms 自动重置、(6) 颜色记忆：回忆阶段底部调色板强制随机打乱防位置记忆、(7) deltaE 下限 10→15 确保高轮次可感知色差、(8) 成就墙：加载时立即展示 14 张占位卡片再异步填充、(9) 签到：网络错误提示开启"不校验合法域名"、(10) 新手引导：集成 tutorial-overlay 含计分规则说明、按模式记录已读状态
