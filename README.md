# Welcome to CNB Cloud Dev 👋

欢迎使用 CNB 云开发环境！这是一个为你准备好的云端开发工作空间。

## 🚀 CNB 平台简介

CNB（Cloud Native Builder）是一个现代化的云端开发平台，提供以下核心功能：

### 核心特性

- **☁️ 云端开发环境** - 在浏览器中即可获得完整的开发环境，无需本地配置
- **🔧 开发容器** - 基于 Docker 容器的隔离环境，预装常用开发工具
- **🌐 公网访问** - 一键将本地服务暴露到公网，方便预览和分享
- **🤖 AI 辅助编程** - 内置 AI 助手，帮助你编写、调试和优化代码
- **📦 项目模板** - 提供多种项目模板，快速启动新项目
- **🔄 Git 集成** - 无缝连接 GitHub/GitLab 等代码托管平台

---

## 📖 cnb-cli 使用指南

`cnb-cli` 是 CNB 平台的命令行工具，让你更高效地管理云端开发环境。

### 常用命令

#### 查看帮助
```bash
cnb --help
cnb <command> --help
```

#### 端口转发（将本地服务暴露到公网）
```bash
# 转发单个端口
cnb forward <port>

# 示例：转发前端开发服务器
cnb forward 3000
cnb forward 8080
```

#### 浏览器自动化
```bash
# 启动浏览器容器（用于截图、测试等）
cnb browser start

# 查看浏览器状态
cnb browser status

# 停止浏览器
cnb browser stop
```

#### 工作空间管理
```bash
# 查看当前工作空间信息
cnb workspace info

# 列出工作空间
cnb workspace list
```

### 实用场景

| 场景 | 命令 |
|------|------|
| 预览 React/Vue 项目 | `cnb forward 3000` |
| 预览静态文件服务器 | `cnb forward 8080` |
| 分享 API 服务 | `cnb forward 3001` |
| 运行端到端测试 | `cnb browser start` |

---

## 🎯 快速开始

### 1. 启动一个简单的开发服务器

```bash
# Python 简单服务器
python -m http.server 8080

# Node.js 项目
npm install
npm run dev
```

### 2. 获取公网访问地址

```bash
cnb forward 3000  # 或你的服务端口
```

### 3. 开始编码

在左侧文件浏览器中选择文件，或使用终端进行开发。

---

## 💡 小贴士

- 💾 你的代码会自动保存在云端，刷新页面不会丢失
- 🔗 使用 `cnb forward` 获得的公网链接可以分享给他人预览
- 📱 支持移动端访问，随时随地查看你的项目
- 🎨 AI 助手可以帮你写代码、调试问题、解释代码逻辑

---

## 📚 更多资源

- [CNB 官方文档](https://cnb.cool/docs)
- [常见问题](https://cnb.cool/faq)
- [更新日志](https://cnb.cool/changelog)

---

<div align="center">

**Happy Coding! 🎉**

如有问题，随时向 AI 助手提问。

</div>
