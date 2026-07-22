# Contributing Guide - Team Collaboration

## Quick Start for Team Members

### 1. Install CLI tools

```bash
brew install cnb gh
```

### 2. Authenticate

```bash
cnb login          # login to CNB
gh auth login      # login to GitHub
```

### 3. Set your identity

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

### 4. Clone & Setup

```bash
git clone https://cnb.cool/buzhi/ZMU/Introduction.git
cd Introduction
./scripts/setup-sync.sh   # configure dual-push remotes
```

### 5. Workflow

```bash
git add .
git commit -m "your changes"
git push origin main      # pushes to BOTH CNB & GitHub
```

## Role Management

| Role | CNB Permission | GitHub Permission |
|------|---------------|-------------------|
| Maintainer | Organization Owner | Admin |
| Developer | Write | Write |
| Contributor | Read (via fork/PR) | Read (via fork/PR) |

### Adding a Team Member

1. **CNB**: Go to `buzhi/ZMU` → Members → Add member
2. **GitHub**: Go to `AdventureX-26-ZMU-Studio/Intro` → Settings → Collaborators → Add

## Sync Pipeline

- On every push to `main`, both pipelines check the counterpart repo
- If out of sync, a `sync/<platform>-<sha>` branch is created as a bookmark
- Both pipelines are configured in `.sync-config` — edit it when forking

## For Fork Users

1. Fork the repo on both CNB and GitHub
2. Run `./scripts/setup-sync.sh` and enter your fork URLs
3. Commit the updated `.sync-config`
4. Add your `CNB_TOKEN` to GitHub Actions secrets
