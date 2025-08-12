# 如何发布新版本

## 自动发布 (推荐)

发布新版本最简单的方法是通过**自动语义化发布**。只需使用正确的提交消息格式进行提交和推送，其他一切都会自动发生。

### 提交消息格式

使用这些前缀来控制发布的类型：

```bash
fix: 解决 CLI 参数解析错误      # → 补丁发布 (4.1.0 → 4.1.1)
feat: 添加新的代理编排模式     # → 次要版本发布 (4.1.0 → 4.2.0)
feat!: 重新设计 CLI 界面              # → 主要版本发布 (4.1.0 → 5.0.0)
```

### 自动发生什么

当您推送带有 `fix:` 或 `feat:` 的提交时，GitHub Actions 将会：

1.  ✅ 分析您的提交消息
2.  ✅ 在 `package.json` 中提升版本
3.  ✅ 生成变更日志
4.  ✅ 创建 git 标签
5.  ✅ **自动发布到 NPM**
6.  ✅ 创建带有说明的 GitHub 版本

### 您简单的流程

```bash
# 进行您的更改
git add .
git commit -m "feat: add team collaboration mode"
git push

# 就是这样！发布会自动发生 🎉
# 用户现在可以运行：npx bmad-method (并获取新版本)
```

### 不会触发发布的提交

这些提交类型不会创建发布 (可用于维护)：

```bash
chore: 更新依赖     # 无发布
docs: 修复 readme 中的拼写错误      # 无发布
style: 格式化代码            # 无发布
test: 添加单元测试          # 无发布
```

### 测试您的设置

```bash
npm run release:test    # 可在本地安全运行 - 测试配置
```

---

## 手动发布方法 (仅限例外情况)

⚠️ 仅在需要绕过自动系统时使用这些方法

### 快速手动版本提升

```bash
npm run version:patch   # 4.1.0 → 4.1.1 (错误修复)
npm run version:minor   # 4.1.0 → 4.2.0 (新功能)
npm run version:major   # 4.1.0 → 5.0.0 (破坏性更改)

# 然后手动发布：
npm publish
git push && git push --tags
```

### 手动触发 GitHub Actions

如果需要，您还可以通过 GitHub Actions 工作流调度手动触发发布。