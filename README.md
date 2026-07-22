# ZMU Introduction

CNB + GitHub 双备份标准仓库。Fork 即用，`git push origin` 一次推到两个远端。

## Quick Setup

```bash
# 1. 安装 CLI
brew install cnb gh

# 2. 登录双端
cnb login && gh auth login

# 3. 配置身份
git config --global user.name "Your Name"
git config --global user.email "you@example.com"

# 4. 克隆并配置
git clone https://cnb.cool/buzhi/ZMU/Introduction.git
cd Introduction
./scripts/setup-sync.sh
```

之后 `git push origin main` 同时推送到 CNB 和 GitHub。

## Sync Pipeline

| 触发端 | 检查端 | 差异时 |
|--------|--------|--------|
| CNB push | GitHub | CNB 创建 `sync/github-<sha>` 分支 |
| GitHub push | CNB | GitHub 创建 `sync/cnb-<sha>` 分支 |

配置文件：`.sync-config`  
CNB 管道：`.cnb.yml`  
GitHub 管道：`.github/workflows/sync-check.yml`

## For Fork Users

1. 在 CNB 和 GitHub 上分别 fork 本仓库
2. 运行 `./scripts/setup-sync.sh`，输入你 fork 后的仓库地址
3. 提交 `.sync-config` 的改动
4. 在 GitHub Settings → Secrets 中添加 `CNB_TOKEN`

## Team Collaboration

详见 [CONTRIBUTING.md](./CONTRIBUTING.md)
