<p align="center">
  <img src="https://img.shields.io/github/v/release/qian-lou/chat2prompt-free?style=flat-square&color=blue" alt="Release" />
  <img src="https://img.shields.io/github/downloads/qian-lou/chat2prompt-free/total?style=flat-square&color=green" alt="Downloads" />
  <img src="https://img.shields.io/badge/platforms-macOS%20%7C%20Windows%20%7C%20Linux-lightgrey?style=flat-square" alt="Platforms" />
  <img src="https://img.shields.io/badge/license-proprietary-orange?style=flat-square" alt="License" />
</p>

<h1 align="center">✨ Chat2Prompt</h1>

<p align="center">
  <strong>AI 结构化提示词生成器 — 免费桌面客户端</strong><br/>
  <em>将你的想法一键转化为专业级 AI 提示词</em>
</p>

<p align="center">
  <a href="https://github.com/qian-lou/chat2prompt-free/releases/latest">📥 立即下载</a> ·
  <a href="#功能特性">功能特性</a> ·
  <a href="#快速开始">快速开始</a> ·
  <a href="#常见问题">FAQ</a>
</p>

---

## 🎯 这是什么？

**Chat2Prompt** 是一款开箱即用的桌面端 AI 提示词生产力工具。只需输入你的想法，选择参数，系统即可自动生成**结构化、专业级**的提示词，适用于：

- 🎨 **图像生成** — Midjourney / DALL·E / Stable Diffusion
- ✍️ **文案创作** — 营销文案 / 品牌介绍 / 内容运营
- 🎬 **视频生成** — Sora / Runway / Kling

> 💡 告别"大白话"提示词，让 AI 输出更专业、更稳定的结果。

---

## ✨ 功能特性

| 功能 | 说明 |
|------|------|
| 🧠 **智能 Prompt 生成** | 输入目标 → 自动生成结构化专业提示词 |
| 🤖 **AI 润色增强** | 对接你自己的 LLM API Key，一键深度优化提示词 |
| 🎨 **多类型支持** | 图像 / 文案 / 视频三大类型，预设丰富参数面板 |
| 📚 **模板库管理** | 收藏精调后的提示词为模板，随时复用 |
| 📜 **历史记录** | 所有生成记录本地保存，支持搜索与收藏 |
| 🔌 **灵活 LLM 配置** | 支持 OpenAI / Claude / DeepSeek / 智谱等多家模型 |
| 🔒 **100% 本地隐私** | 数据完全存储于本地 SQLite，绝不上传任何信息 |
| 🌙 **暗色主题** | 精致的深色界面，长时间使用不疲劳 |
| 🖥️ **跨平台** | macOS (Apple Silicon) / Windows / Linux |

---

## 📥 快速开始

### 1. 下载安装

前往 [**Releases 页面**](https://github.com/qian-lou/chat2prompt-free/releases/latest) 下载对应平台的安装包：

| 平台 | 文件格式 |
|------|---------|
| macOS (Apple Silicon M1/M2/M3/M4) | `.dmg` |
| Windows | `.msi` / `.exe` |
| Linux | `.deb` / `.AppImage` |

### 2. 使用方式

1. **打开应用** — 进入默认生成面板
2. **输入想法** — 如"做一张复古手绘风的信息图，讲前端编程发展历史"
3. **选择参数** — 输出类型、视觉风格、画面比例、细节等级
4. **点击生成** — 系统自动输出结构化提示词

### 3. (可选) 配置 AI 润色

1. 打开 **设置** 页面
2. 添加 LLM Provider（填入 Base URL、API Key、模型名）
3. 返回生成页，开启 **AI 润色增强** 开关
4. 生成时系统会调用你的 LLM 对提示词进行深度优化

> 🔑 支持所有兼容 OpenAI 接口的服务：OpenAI、Anthropic Claude、DeepSeek、智谱 AI、通义千问、本地部署的 Ollama 等。

---

## 🤔 常见问题

<details>
<summary><strong>不配置 API Key 能用吗？</strong></summary>

可以！系统内置了本地模板引擎，无需 API Key 即可生成结构化提示词。AI 润色是**可选的增强功能**。
</details>

<details>
<summary><strong>我的数据安全吗？</strong></summary>

完全安全。所有模板、历史记录、API Key 均存储在本地 SQLite 数据库中（`~/.chat2prompt/data.db`），应用不会向任何服务器上传数据（除非你主动调用 LLM API）。
</details>

<details>
<summary><strong>支持哪些大模型？</strong></summary>

支持所有兼容 OpenAI Chat Completions API 的模型，包括：
- OpenAI GPT-4o / GPT-4o-mini
- Anthropic Claude 3.5 / Claude 3 (使用 Messages API)
- DeepSeek Chat / DeepSeek Reasoner
- 智谱 AI GLM-4
- 通义千问 Qwen
- 本地部署的 Ollama、vLLM 等
</details>

<details>
<summary><strong>macOS 提示"无法验证开发者"？</strong></summary>

由于应用未经 Apple 公证签名，首次打开时可能被 Gatekeeper 阻止：
1. 打开 **系统设置 → 隐私与安全性**
2. 找到被阻止的 Chat2Prompt，点击 **仍要打开**

或使用终端：
```bash
xattr -cr /Applications/Chat2Prompt.app
```
</details>

---

## 📋 更新日志

### v0.1.1 (2025-03-25)
- 🐛 修复 Python sidecar 在打包后崩溃的问题
- 🐛 修复 WebKit fetch 错误匹配

### v0.1.0 (2025-03-24)
- 🎉 首个发布版本
- ✨ 支持图像/文案/视频三种类型的结构化提示词生成
- ✨ 集成 LLM AI 润色功能
- ✨ 本地模板库与历史记录管理
- ✨ 跨平台桌面客户端 (macOS / Windows / Linux)

---

## 📄 许可证

本软件为**个人免费使用，禁止商业用途**（Personal Use Only）。

- ✅ 个人免费下载和使用
- ✅ 个人学习和非商业项目
- ❌ **禁止任何商业用途**（包括企业内部使用）
- ❌ 不得反编译、逆向工程或修改
- ❌ 不得重新分发修改版本

如需商业授权，请联系作者。

Copyright © 2025 Chat2Prompt. All rights reserved.
