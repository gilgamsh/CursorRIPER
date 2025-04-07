![CursorRIPER](./res/github-header.png)
# CursorRIPER 框架 - @ 符号增强功能

本自述文件包含 CursorRIPER 框架的 @ 符号增强分支的实现。此增强功能在整个框架中集成了 Cursor IDE 强大的 @ 符号功能，以改进上下文引用，同时保留核心 RIPER 工作流。

## 目录结构

```
CursorRIPER/
├── src/
│   ├── .cursor/
│   │   └── rules/
│   │       ├── core.mdc                  # 更新了 @ 符号检测和建议
│   │       ├── state.mdc                 # 更新了 @ 符号状态跟踪
│   │       ├── start-phase.mdc           # 更新了渐进式符号引入
│   │       ├── riper-workflow.mdc        # 更新了模式特定符号指导
│   │       └── customization.mdc         # 更新了符号自定义选项
│   └── templates/
│       └── memory-bank/
│           └── @-symbol-registry.md      # 新增：符号注册表模板
└── docs/
    └── @-symbol-guide.md                # 新增：全面的符号使用指南
```

## 实现细节

该增强功能在整个 CursorRIPER 框架中添加了 @ 符号集成：

1. **核心框架更新**：
   - 符号检测和建议规则
   - 符号注册表状态跟踪
   - 性能优化指导
   - 自定义选项

2. **START 阶段集成**：
   - 在每个步骤中渐进地引入符号
   - 符号发现和注册表设置

3. **RIPER 工作流集成**：
   - 模式特定符号推荐
   - 跨模式一致性指南
   - 符号特定内存库更新

4. **内存库增强功能**：
   - 全面的符号注册表模板
   - 所有内存库模板中的符号部分

5. **文档**：
   - 带有可视化图表的详细使用指南
   - 最佳实践和故障排除
   - 项目类型特定建议

## 安装

要在现有 CursorRIPER 项目中实现此增强功能：

1. 备份现有框架文件：
   ```
   mkdir -p .backup/$(date +%Y-%m-%d)
   cp -r .cursor/rules/* .backup/$(date +%Y-%m-%d)/
   ```

2. 复制更新的框架文件：
   ```
   cp -r implementation/src/.cursor/rules/* .cursor/rules/
   ```

3. 复制新的内存库模板：
   ```
   cp implementation/src/templates/memory-bank/@-symbol-registry.md memory-bank/
   ```

4. 复制新文档：
   ```
   cp implementation/docs/@-symbol-guide.md docs/
   ```

5. 初始化 @ 符号注册表：
   - 如果在 START 阶段：将在步骤 6 中创建注册表
   - 如果在 DEVELOPMENT 或 MAINTENANCE 阶段：根据模板手动创建注册表

## 使用方法

参考 `@-symbol-guide.md` 获取全面的使用说明。

每种模式的基本使用模式：

- **RESEARCH（研究）**：使用 `@Files`，`@Folders` 和 `@Code` 探索代码库
- **INNOVATE（创新）**：使用 `@Web` 和 `@Docs` 研究解决方案
- **PLAN（计划）**：在计划中使用精确的 `@Files` 和 `@Code` 引用
- **EXECUTE（执行）**：在实施过程中引用计划中的符号
- **REVIEW（审查）**：使用符号比较已实施的文件与计划的目标

## 故障排除

如果遇到问题：

1. 验证 state.mdc 是否已适当更新，包含 @ 符号状态跟踪
2. 确保 @-symbol-registry.md 存在于内存库中
3. 检查 customization.mdc 是否有正确的符号偏好设置
4. 参考 @-symbol-guide.md 中的故障排除部分

## 版权
---

## 许可证

MIT 许可证 - 详见根目录中的 LICENSE 文件。 