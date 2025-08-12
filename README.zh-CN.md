# BMad-Method：通用人工智能代理框架

[![版本](https://img.shields.io/npm/v/bmad-method?color=blue&label=version)](https://www.npmjs.com/package/bmad-method)
[![许可证: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Node.js 版本](https://img.shields.io/badge/node-%3E%3D20.0.0-brightgreen)](https://nodejs.org)
[![Discord](https://img.shields.io/badge/Discord-Join%20Community-7289da?logo=discord&logoColor=white)](https://discord.gg/gk8jAdXWmj)

BMad-Method 源于“敏捷AI驱动开发的突破性方法”（Breakthrough Method of Agile AI-Driven Development），但其内涵远不止于此。它能将专业化的AI能力应用到任何领域，无论是软件开发、娱乐、创意写作、商业策略，还是个人健康等等，都能大显身手。

**[在YouTube上订阅BMadCode](https://www.youtube.com/@BMadCode?sub_confirmation=1)**

**[加入我们的Discord社区](https://discord.gg/gk8jAdXWmj)** - 一个为AI爱好者打造的成长型社区！在这里，你可以获取帮助、分享想法、探索AI代理与框架、协作技术项目、享受共同爱好，并互相帮助取得成功。无论你是在BMad上遇到了困难，还是在构建自己的代理，或者只是想聊聊最新的AI动态——我们都在这里为你服务！**部分移动设备和VPN用户可能在加入Discord时遇到问题，这是Discord自身的问题——如果邀请链接无效，请尝试使用你自己的网络、其他网络或关闭VPN后重试。**

⭐ **如果你觉得这个项目对你有帮助，请在右上角点亮星星！** 这能帮助更多人发现BMad-Method，你也会收到项目更新的通知！

## 概述

**BMad Method的两大核心创新：**

**1. 代理驱动的规划：** 专属的代理（分析师、项目经理、架构师）与你协作，创建详尽且一致的产品需求文档（PRD）和架构文档。通过先进的提示工程和“人在环路”的优化，这些规划代理能够生成远超通用AI任务生成的全面规范。

**2. 上下文工程化的开发：** Scrum Master代理随后将这些详细的计划转化为超详细的开发故事（Development Stories），其中包含了开发代理所需的一切——完整的上下文、实现细节和架构指导，都直接嵌入在故事文件中。

这种两阶段方法解决了AI辅助开发中的两大难题——**规划不一致**和**上下文丢失**。你的开发代理在打开一个故事文件时，就能完全理解要构建什么、如何构建以及为何构建。

**📖 [在用户指南中查看完整工作流程](docs/user-guide.md)** - 了解规划阶段、开发周期和所有代理的角色。

## 快速导航

### 理解BMad工作流程

**在开始之前，请务必查看这些关键的工作流程图，它们解释了BMad的运作方式：**

1.  **[规划工作流程 (Web UI)](docs/user-guide.md#the-planning-workflow-web-ui)** - 如何创建产品需求文档（PRD）和架构文档
2.  **[核心开发周期 (IDE)](docs/user-guide.md#the-core-development-cycle-ide)** - Scrum Master、开发和QA代理如何通过故事文件进行协作

> ⚠️ **这些图表解释了BMad方法中90%的关于“代理式敏捷流程”的困惑** - 理解PRD和架构的创建过程，以及SM/Dev/QA的工作流程，还有代理如何通过故事文件传递信息至关重要——这也解释了为什么BMad不仅仅是一个任务管理器或简单的任务执行器！

### 你想做什么？

- **[安装并使用全栈敏捷AI团队构建软件](#快速入门)** → 快速入门指南
- **[学习如何使用BMad](docs/user-guide.md)** → 完整的用户指南和演练
- **[查看可用的AI代理](/bmad-core/agents))** → 为你的团队配置专业角色
- **[探索非技术用途](#-超越软件开发---扩展包)** → 创意写作、商业、健康、教育
- **[创建我自己的AI代理](docs/expansion-packs.md)** → 为你的领域构建专属代理
- **[浏览现成的扩展包](expansion-packs/)** → 游戏开发、DevOps、基础设施，并从中获取灵感和示例
- **[理解其架构](docs/core-architecture.md)** → 技术深度剖析
- **[加入社区](https://discord.gg/gk8jAdXWmj)** → 获取帮助和分享想法

## 重要提示：保持你的BMad安装为最新版本

**轻松保持更新！** 如果你的项目中已经安装了BMad-Method，只需运行：

```bash
npx bmad-method install
# 或者
git pull
npm run install:bmad
```

此命令将：

- ✅ 自动检测你现有的v4安装
- ✅ 只更新已更改的文件并添加新文件
- ✅ 为你做出的任何自定义修改创建`.bak`备份文件
- ✅ 保留你项目特定的配置

这让你能轻松受益于最新的改进、错误修复和新代理，而不会丢失你的自定义设置！

## 快速入门

### 一键完成所有操作（IDE安装）

**只需运行以下命令之一：**

```bash
npx bmad-method install
# 或者，如果你已经安装了BMad：
git pull
npm run install:bmad
```

这个单一命令可以处理：

- **新安装** - 在你的项目中设置BMad
- **升级** - 自动更新现有安装
- **扩展包** - 安装你已添加到`package.json`中的任何扩展包

> **就是这样！** 无论你是首次安装、升级还是添加扩展包——这些命令都能搞定一切。

**先决条件**：需要 [Node.js](https://nodejs.org) v20+

### 最快上手：Web UI全栈团队随时待命（2分钟）

1.  **获取团队包**：保存或克隆[全栈团队文件](dist/teams/team-fullstack.txt)或选择另一个团队
2.  **创建AI代理**：创建一个新的Gemini Gem或CustomGPT
3.  **上传并配置**：上传文件并设置指令：“你附带了关键操作指令，请严格按照指示扮演角色”
4.  **开始构思和规划**：开始聊天！输入`*help`查看可用命令，或选择一个代理，如`*analyst`，直接开始创建简报。
5.  **关键**：随时在Web界面与BMad Orchestrator（#bmad-orchestrator命令）交谈，询问关于这一切如何运作的问题！
6.  **何时转向IDE**：一旦你有了PRD、架构、可选的UX和简报——就该切换到IDE来对你的文档进行分片，并开始实现实际代码了！更多详情请参阅[用户指南](docs/user-guide.md)。

### 替代方案：克隆并构建

```bash
git clone https://github.com/bmadcode/bmad-method.git
npm run install:bmad # 构建并安装所有内容到目标文件夹
```

## 🌟 超越软件开发 - 扩展包

BMad的自然语言框架适用于任何领域。扩展包为创意写作、商业策略、健康与保健、教育等领域提供了专门的AI代理。此外，扩展包还可以为核心BMad-Method添加非通用的特定功能。[查看扩展包指南](docs/expansion-packs.md)并学习创建你自己的扩展包！

## 代码库扁平化工具

BMad-Method包含一个强大的代码库扁平化工具，旨在为AI模型准备你的项目文件。该工具将你的整个代码库聚合到一个XML文件中，使你可以轻松地与AI助手共享项目上下文，以进行分析、调试或开发辅助。

### 功能

- **AI优化输出**：生成专为AI模型消费而设计的纯净XML格式
- **智能过滤**：自动遵循`.gitignore`模式，排除不必要的文件
- **二进制文件检测**：智能识别并排除二进制文件，专注于源代码
- **进度跟踪**：实时进度指示器和全面的完成统计
- **灵活输出**：可自定义输出文件的位置和名称

### 用法

```bash
# 基本用法 - 在当前目录创建 flattened-codebase.xml
npx bmad-method flatten

# 指定自定义输入目录
npx bmad-method flatten --input /path/to/source/directory
npx bmad-method flatten -i /path/to/source/directory

# 指定自定义输出文件
npx bmad-method flatten --output my-project.xml
npx bmad-method flatten -o /path/to/output/codebase.xml

# 结合输入和输出选项
npx bmad-method flatten --input /path/to/source --output /path/to/output/codebase.xml
```

### 输出示例

该工具将显示进度并提供全面的摘要：

```text
📊 完成摘要:
✅ 成功将 156 个文件处理到 flattened-codebase.xml
📁 输出文件: /path/to/your/project/flattened-codebase.xml
📏 源文件总大小: 2.3 MB
📄 生成的XML大小: 2.1 MB
📝 总代码行数: 15,847
🔢 预估Token数: 542,891
📊 文件明细: 142 个文本文件, 14 个二进制文件, 0 个错误
```

生成的XML文件以结构化格式包含你项目的基于文本的源文件，AI模型可以轻松解析和理解，非常适合代码审查、架构讨论或在你的BMad-Method项目中获得AI辅助。

#### 高级用法与选项

- CLI选项
  - `-i, --input <path>`：要扁平化的目录。默认值：当前工作目录，或在交互模式下自动检测到的项目根目录。
  - `-o, --output <path>`：输出文件路径。默认值：在所选目录中生成`flattened-codebase.xml`。
- 交互模式
  - 如果你没有传递`--input`和`--output`并且终端是交互式的（TTY），该工具将尝试检测你的项目根目录（通过查找`.git`、`package.json`等标记）并提示你确认或覆盖路径。
  - 在非交互式上下文（例如CI）中，它将静默地优先使用检测到的根目录；否则，它将回退到当前目录和默认文件名。
- 文件发现和忽略
  - 在git仓库内时使用`git ls-files`以提高速度和准确性；否则回退到基于glob的扫描。
  - 应用你的`.gitignore`以及一组精选的默认忽略模式（例如，`node_modules`、构建输出、缓存、日志、IDE文件夹、锁文件、大型媒体/二进制文件、`.env*`以及先前生成的XML输出）。
- 二进制文件处理
  - 检测并从XML内容中排除二进制文件。它们会在最终摘要中计数，但不会嵌入到输出中。
- XML格式和安全性
  - 使用UTF-8编码的XML文件，根元素为`<files>`。
  - 每个文本文件都作为`<file path="relative/path">`元素发出，其内容包裹在`<![CDATA[ ... ]]>`中。
  - 该工具通过拆分CDATA来安全地处理内容中出现的`]]>`，以保持正确性。
  - 文件内容按原样保留，并在XML内部进行缩进以提高可读性。
- 性能
  - 根据你的CPU和工作负载大小自动选择并发级别。无需配置。
  - 在git仓库内运行可提高发现性能。

#### 最小XML示例

```xml
<?xml version="1.0" encoding="UTF-8"?>
<files>
  <file path="src/index.js"><![CDATA[
    // 你的源代码内容
  ]]></file>
</files>
```

## 文档与资源

### 核心指南

- 📖 **[用户指南](docs/user-guide.md)** - 从项目构想到完成的完整演练
- 🏗️ **[核心架构](docs/core-architecture.md)** - 技术深度剖析和系统设计
- 🚀 **[扩展包指南](docs/expansion-packs.md)** - 将BMad扩展到软件开发之外的任何领域

## 支持

- 💬 [Discord社区](https://discord.gg/gk8jAdXWmj)
- 🐛 [问题跟踪](https://github.com/bmadcode/bmad-method/issues)
- 💬 [讨论区](https://github.com/bmadcode/bmad-method/discussions)

## 贡献

**我们热切欢迎各种贡献，并期待你的想法、改进和扩展包！** 🎉

📋 **[阅读CONTRIBUTING.md](CONTRIBUTING.md)** - 完整的贡献指南，包括准则、流程和要求。

## 许可证

MIT许可证 - 详情请参阅[LICENSE](LICENSE)文件。

[![贡献者](https://contrib.rocks/image?repo=bmadcode/bmad-method)](https://github.com/bmadcode/bmad-method/graphs/contributors)

<sub>用❤️为AI辅助开发社区构建</sub>