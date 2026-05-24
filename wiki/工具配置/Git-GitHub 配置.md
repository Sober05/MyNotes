# Git-GitHub 配置

## 当前状态

- **Git 版本：** 2.54.0（已安装）
- **全局配置：** ❌ 未配置（name / email）
- **GitHub 认证：** ❌ 未登录（gh auth）

## 待完成

- [ ] 配置 `git config --global user.name`
- [ ] 配置 `git config --global user.email`
- [ ] 登录 GitHub：`gh auth login`
- [ ] 创建 GitHub 仓库用于 Vault 同步
- [ ] 初始化 `MyNotes` 为 Git 仓库并 push

## 参考命令

```bash
# 配置用户信息
git config --global user.name "你的名字"
git config --global user.email "你的邮箱"

# 登录 GitHub
gh auth login

# 初始化仓库
cd MyNotes
git init
git add -A
git commit -m "init: Obsidian vault"
git remote add origin <repo-url>
git push -u origin main
```
