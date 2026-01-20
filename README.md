# SQLHunter

<p align="center">
  <img src="docs/logo.png" alt="SQLHunter Logo" width="400">
</p>

<p align="center">
  <b>一款简洁高效的 SQL 注入检测与利用工具</b>
</p>

<p align="center">
  <a href="#功能特性">功能特性</a> •
  <a href="#安装">安装</a> •
  <a href="#快速开始">快速开始</a> •
  <a href="https://robot0p.github.io/SQLHunter/guide.html">在线文档</a>
</p>

<p align="center">
  中文 | <a href="README-EN.md">English</a>
</p>

---

<p align="center">
  <img src="docs/screenshots/main-interface.png" alt="SQLHunter Main Interface" width="100%">
</p>

---

## 功能特性

### 智能扫描
- **一键扫描**: 输入目标 URL，自动检测 SQL 注入漏洞
- **批量扫描**: 支持导入多个目标进行批量测试
- **任务队列**: 自动管理扫描任务，支持并发控制
- **实时输出**: 查看扫描过程的实时日志和进度

### 高级配置
- **智能配置面板**: 可视化配置所有 sqlmap 参数
- **预设管理**: 保存常用配置为预设，一键加载
- **目标管理器**: 管理多个目标，支持分组和标签
- **Payload 管理**: 自定义和管理注入 Payload

### 代理支持
- **智能代理池**: 自动获取和管理代理，支持自动轮换
- **代理验活**: 定期检测代理可用性
- **Tor 集成**: 一键启动 Tor，支持身份切换
- **链路可视化**: 实时显示 Tor 链路节点和国家信息

<p align="center">
  <img src="docs/screenshots/proxy-pool.png" alt="Smart Proxy Pool" width="80%">
  <br>
  <em>智能代理池 - 代理管理与 Tor 集成</em>
</p>

### 结果分析
- **AI 分析**: 智能分析扫描结果，提供漏洞评估
- **数据库结构树**: 可视化显示获取的数据库结构
- **报告导出**: 支持导出扫描报告

### 界面体验
- **多主题支持**: 8 款精美主题，包括赛博朋克、矩阵、霓虹等
- **中英双语**: 完整的中英文界面支持
- **跨平台**: 支持 Windows、macOS、Linux

---

## 安装

### 系统要求
- **操作系统**: Windows 10+、macOS 10.13+、Linux (Ubuntu 18.04+)
- **依赖**: Python 3.x、sqlmap

### 下载安装

从 [Releases](https://github.com/Robot0P/SQLHunter/releases) 页面下载适合你系统的安装包：

| 平台 | 文件 |
|------|------|
| Windows | `SQLHunter_x.x.x_x64-setup.exe` |
| macOS | `SQLHunter_x.x.x_x64.dmg` |
| Linux | `SQLHunter_x.x.x_amd64.deb` |

### 环境检测

首次启动时，应用会自动检测依赖环境：
- 已安装的依赖会显示绿色勾号
- 缺失的依赖可点击「一键修复」自动安装

---

## 快速开始

### 1. 基本扫描

1. 在顶部输入框中输入目标 URL（包含注入点参数）
   ```
   http://example.com/page.php?id=1
   ```
2. 点击「开始扫描」按钮
3. 在「输出」面板查看实时扫描结果

### 2. 使用代理

1. 点击右上角的「代理池」图标
2. 在「代理源」标签页添加代理获取源
3. 点击「获取代理」自动获取代理列表
4. 启用「智能代理池」开关

### 3. 使用 Tor

1. 打开「代理池」面板
2. 切换到「Tor」标签页
3. 点击「启动 Tor」按钮
4. 查看 Tor 链路节点和出口 IP

---

## 使用指南

### 目标管理

- **添加目标**: 点击「+」按钮添加新目标
- **批量导入**: 支持从文件或剪贴板导入多个 URL
- **分组管理**: 为目标创建分组，方便管理
- **标签标记**: 使用标签对目标进行分类

### 配置面板

配置面板分为多个区域：

| 区域 | 功能 |
|------|------|
| 目标设置 | URL、数据、Cookie 等 |
| 检测选项 | 检测级别、风险等级 |
| 注入技术 | 选择注入技术类型 |
| 枚举选项 | 数据库、表、列枚举 |
| 高级选项 | 代理、线程、超时等 |

### 快捷键

| 快捷键 | 功能 |
|--------|------|
| `Ctrl/Cmd + Enter` | 开始扫描 |
| `Ctrl/Cmd + .` | 停止扫描 |
| `Ctrl/Cmd + ,` | 打开设置 |
| `Ctrl/Cmd + L` | 清除输出 |

---

## 主题

内置 8 款精美主题：

- **赛博朋克** - 霓虹粉紫色调
- **隐匿模式** - 深邃暗色调
- **矩阵** - 经典绿色终端风格
- **霓虹** - 亮丽紫色
- **浅色** - 明亮简洁
- **午夜蓝** - 深蓝夜空
- **德古拉** - 经典暗色
- **莫诺凯** - 代码编辑器风格

---

## 常见问题

### Q: 扫描时提示「sqlmap 未安装」？
A: 点击设置中的「环境检测」，然后点击「一键修复」自动安装 sqlmap。

### Q: 如何使用 Burp Suite 的请求？
A: 在 Burp 中复制请求，然后在配置面板的「请求」部分粘贴完整请求内容。

### Q: Tor 无法启动？
A: 请先确保已安装 Tor：
- macOS: `brew install tor`
- Linux: `sudo apt install tor`
- Windows: 下载安装 Tor Expert Bundle

### Q: 如何添加自定义代理源？
A: 在「代理池」→「代理源」中添加返回 `ip:port` 格式的 URL。

---

## 更新日志

### v1.0.0 (2026-01-20)

**首次发布**

- 智能扫描引擎，支持多种注入技术
- 智能代理池，自动获取和轮换代理
- Tor 网络集成，一键启动和身份切换
- 可视化配置面板，支持预设管理
- AI 智能分析扫描结果
- 8 款精美主题
- 中英双语界面
- 跨平台支持（Windows、macOS、Linux）

---

## 免责声明

本工具仅供安全研究和授权测试使用。使用本工具进行未授权的测试是违法的。用户需自行承担使用本工具的所有法律责任。

---

<p align="center">
  <sub>Made with love for Security Researchers</sub>
</p>
