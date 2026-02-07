# 📝 Markdown 在线编辑器

一个轻量级、功能强大的 Markdown 在线编辑器，支持实时预览、Mermaid 图表和导出功能。

![GitHub License](https://img.shields.io/badge/license-MIT-green.svg)
![GitHub Stars](https://img.shields.io/github/stars/ZBIGBEAR/md.svg)
![GitHub Forks](https://img.shields.io/github/forks/ZBIGBEAR/md.svg)

## ✨ 功能特性

- **实时预览**：左侧编辑器，右侧实时预览，所见即所得
- **工具栏快捷插入**：一键插入粗体、斜体、标题、引用、代码块等常用格式
- **Mermaid 图表**：支持流程图、序列图、类图、状态图四种图表类型
- **拖拽调整**：通过拖拽分割线自定义编辑器和预览比例
- **导出功能**：
  - 导出为 Markdown (.md) 文件
  - 导出为 PDF (.pdf) 文件（支持多页）
- **快捷键支持**：`Ctrl/Cmd + B` 加粗、`Ctrl/Cmd + I` 斜体等
- **悬浮菜单**：可隐藏工具栏，提供更多快捷操作
- **响应式设计**：完美支持移动端和桌面端

## 📦 快速开始

### 直接运行

由于这是一个单文件 HTML 应用，无需任何构建工具，直接在浏览器中打开即可：

```bash
# 直接双击打开 index.html
# 或使用命令行
open index.html
```

### 在线预览

打开 `index.html` 文件，开始编写 Markdown 吧！

## 🎯 使用指南

### 工具栏功能

- **文本格式**：加粗、斜体、标题 (H1-H3)、引用、代码、分隔线
- **列表**：无序列表、有序列表
- **链接和图片**：快速插入 Markdown 链接和图片
- **Mermaid 图表**：四种图表类型的快速插入模板

### 快捷键

| 快捷键 | 功能 |
|--------|------|
| `Ctrl/Cmd + B` | 加粗 |
| `Ctrl/Cmd + I` | 斜体 |
| `Ctrl/Cmd + M` | 插入流程图 |
| `Tab` | 插入空格 |
| `/` | 聚焦光标 |

### 导出功能

点击右下角悬浮菜单按钮（+）可以访问：

- 隐藏/显示工具栏
- 导出 MD 文件
- 导出 PDF 文件（会自动渲染所有 Mermaid 图表）
- 清空编辑器
- 查看快捷键列表
- 打开 Mermaid 和 Markdown 语法参考

### 分割比例调整

- 点击工具栏的分割比例下拉菜单选择：33% / 50% / 66%
- 直接拖拽分割线自定义比例
- 双击分割线恢复默认 50% 比例

## 🛠️ 技术栈

- **Marked.js**：Markdown 解析器
- **Mermaid.js**：图表渲染引擎
- **html2canvas**：PDF 导出截图
- **jsPDF**：PDF 文件生成
- **原生 HTML/CSS/JavaScript**：零依赖，单文件实现

## 📄 许可证

本项目采用 MIT 许可证。详见 [LICENSE](LICENSE) 文件。

## 🤝 贡献

欢迎提交 Issue 和 Pull Request！

## 📊 Stars 趋势

[![Stars Notifier](https://img.shields.io/badge/Stars%20Chart-View%20Stars%20Chart-blue)](https://stars-notifier.netlify.app/dashboard#?repo=ZBIGBEAR/md)

点击上方按钮查看 GitHub Stars 的增长趋势图。

### 如何查看

1. 访问 [Stars Notifier](https://stars-notifier.netlify.app/)
2. 搜索并添加仓库 `ZBIGBEAR/md`
3. 即可查看 Stars 增长曲线图

### 配置 Stars 曲线图

如果你想在仓库中使用 Stars Notifier 自动生成曲线图，可以添加以下 GitHub Actions：

```yaml
# 在仓库 `.github/workflows/notify-stars.yml`
name: Notify Stars
on:
  schedule:
    - cron: '0 0 * * *'  # 每天凌晨 0 点
  workflow_dispatch:
  push:
    branches: [main]
jobs:
  notify:
    runs-on: ubuntu-latest
    steps:
      - uses: orastron/stars-notifier-action@v3.0
        with:
          token: ${{ secrets.GITHUB_TOKEN }}
          org: yourusername
          repo: markdown-editor
          webhook_url: ${{ secrets.STARS_WEBHOOK_URL }}
```

## 📧 联系方式

如有问题或建议，欢迎通过以下方式联系：

- 提交 GitHub Issue
- 发送邮件至 664141154@qq.com

---

Made with ❤️ using pure HTML, CSS, and JavaScript
