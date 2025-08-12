# 如何通过拉取请求 (Pull Request) 做出贡献

**刚接触 GitHub 和拉取请求？** 本指南将带您一步步了解基础知识。

## 什么是拉取请求？

拉取请求 (PR) 是您在 GitHub 上向项目提出变更的方式。可以把它想象成：“我做了一些修改，请审查并考虑将它们合并到主项目中。”

## 开始之前

⚠️ **重要提示**：请保持您的贡献小而专注！我们更喜欢许多小的、清晰的变更，而不是一个庞大的变更。

**提交 PR 前的要求：**

-   **对于错误修复**：使用[错误报告模板](https://github.com/bmadcode/bmad-method/issues/new?template=bug_report.md)创建一个 issue。
-   **对于新功能**：
    1.  在 Discord 的 [#general-dev 频道](https://discord.gg/gk8jAdXWmj)进行讨论。
    2.  使用[功能请求模板](https://github.com/bmadcode/bmad-method/issues/new?template=feature_request.md)创建一个 issue。
-   **对于重大变更**：请务必先创建一个 issue 进行讨论，以确保方向一致。

## 分步指南

### 1. 复刻 (Fork) 仓库

1.  前往 [BMad-Method 仓库](https://github.com/bmadcode/bmad-method)。
2.  点击右上角的“Fork”按钮。
3.  这会创建您自己项目的一份副本。

### 2. 克隆 (Clone) 您的复刻

```bash
# 将 YOUR-USERNAME 替换为您的实际 GitHub 用户名
git clone https://github.com/YOUR-USERNAME/bmad-method.git
cd bmad-method
```

### 3. 创建一个新分支

**永远不要直接在 `main` 分支上工作！** 始终为您的变更创建一个新分支：

```bash
# 创建并切换到一个新分支
git checkout -b fix/typo-in-readme
# 或者
git checkout -b feature/add-new-agent
```

**分支命名技巧：**

-   `fix/description` - 用于错误修复
-   `feature/description` - 用于新功能
-   `docs/description` - 用于文档变更

### 4. 进行您的变更

-   编辑您想要更改的文件。
-   保持变更小而专注，一次只做一件事。
-   如果可能，测试您的变更。

### 5. 提交您的变更

```bash
# 添加您的变更
git add .

# 使用清晰的消息提交
git commit -m "Fix typo in README.md"
```

**好的提交消息：**

-   "Fix typo in installation instructions" (修复安装说明中的拼写错误)
-   "Add example for new agent usage" (为新代理用法添加示例)
-   "Update broken link in docs" (更新文档中的损坏链接)

**不好的提交消息：**

-   "stuff" (东西)
-   "changes" (变更)
-   "update" (更新)

### 6. 推送到您的复刻

```bash
# 将您的分支推送到您的复刻
git push origin fix/typo-in-readme
```

### 7. 创建拉取请求

1.  在 GitHub 上转到您的复刻。
2.  您会看到一个绿色的“Compare & pull request”按钮——点击它。
3.  选择正确的目标分支：
    -   **`next` 分支** 用于大多数贡献 (功能、文档、增强)。
    -   **`main` 分支** 仅用于关键修复。
4.  使用 CONTRIBUTING.md 中的模板填写 PR 描述：
    -   **What (什么)**：1-2 句话描述变更内容。
    -   **Why (为什么)**：1-2 句话解释原因。
    -   **How (如何)**：2-3 个要点说明实现方式。
    -   **Testing (测试)**：您是如何测试的。
5.  引用相关的 issue 编号 (例如，“Fixes #123”)。

### 8. 等待审查

-   维护者将审查您的 PR。
-   他们可能会要求进行更改。
-   请耐心并及时回应反馈。

## 什么是好的拉取请求？

✅ **好的 PRs：**

-   一次只更改一件事。
-   有清晰、描述性的标题。
-   在描述中解释了“什么”和“为什么”。
-   只包含需要更改的文件。

❌ **避免：**

-   更改整个文件的格式。
-   在一个 PR 中进行多个不相关的更改。
-   将您的整个项目/仓库复制到 PR 中。
-   没有解释的更改。

## 要避免的常见错误

1.  **不要重新格式化整个文件** - 只更改必要的部分。
2.  **不要包含不相关的更改** - 每个 PR 只专注于一个修复/功能。
3.  **不要在 issue 中粘贴代码** - 创建一个正式的 PR。
4.  **不要提交您的整个项目** - 贡献具体的改进。

## 需要帮助？

-   💬 加入我们的 [Discord 社区](https://discord.gg/gk8jAdXWmj) 获取实时帮助：
    -   **#general-dev** - 技术问题和功能讨论
    -   **#bugs-issues** - 在提交 issue 前获取有关错误的帮助
-   💬 在 [GitHub Discussions](https://github.com/bmadcode/bmad-method/discussions) 中提问。
-   🐛 使用[错误报告模板](https://github.com/bmadcode/bmad-method/issues/new?template=bug_report.md)报告错误。
-   💡 使用[功能请求模板](https://github.com/bmadcode/bmad-method/issues/new?template=feature_request.md)建议功能。
-   📖 阅读完整的[贡献指南](../CONTRIBUTING.md)。

## 示例：好的 PR vs 坏的 PR

### 😀 好的 PR 示例

**标题**：“修复安装指南的损坏链接”
**变更**：一个文件，一行更改
**描述**：“README.md 中的链接指向了错误的文件。已更新为指向正确的安装指南。”

### 😞 坏的 PR 示例

**标题**：“更新”
**变更**：50 个文件，整个代码库被重新格式化
**描述**：“做了一些改进”

---

**请记住**：我们在这里提供帮助！不要害怕提问。每个专家都曾是初学者。