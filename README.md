# ZMU Introduction

GitHub → CNB 自动镜像。`git push origin` 同时推到两边。

## Quick Setup

```bash
brew install cnb gh
cnb login && gh auth login

git config --global user.name "Your Name"
git config --global user.email "you@example.com"

git clone https://cnb.cool/buzhi/ZMU/Introduction.git
cd Introduction
./scripts/setup-sync.sh
```

## Sync

| 方向 | 方式 |
|------|------|
| GitHub → CNB | 自动：push 时 GitHub Actions 镜像到 CNB |
| CNB → GitHub | 手动：`git push origin main`（双推送） |

配置：`.sync-config` | 流水线：`.github/workflows/sync-check.yml`

## Team

详见 [CONTRIBUTING.md](./CONTRIBUTING.md)
