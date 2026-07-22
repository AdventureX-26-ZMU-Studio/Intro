# Contributing Guide

## Setup

```bash
brew install cnb gh
cnb login && gh auth login

git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

## Clone & Push

```bash
git clone https://cnb.cool/buzhi/ZMU/Introduction.git
cd Introduction
./scripts/setup-sync.sh
```

之后 `git push origin main` → 同时推到 CNB + GitHub。GitHub 收到 push 后也会自动镜像回 CNB。

## Adding Members

- **CNB**: buzhi/ZMU → Members → Add
- **GitHub**: AdventureX-26-ZMU-Studio/Intro → Settings → Collaborators → Add
