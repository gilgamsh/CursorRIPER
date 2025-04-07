![CursorRIPER](../res/github-header.png)
# CursorRIPER 框架 - 安装指南

本指南将帮助您为项目设置 CursorRIPER 框架。

## 前提条件

- 已安装 [Cursor IDE](https://cursor.sh/)
- Git（可选但推荐）
- 对项目需求的基本了解

## 安装

1. **将框架文件复制到您的项目并将文件重命名为 *.mdc**

   在项目根目录中创建一个 `.cursor` 目录并复制必要的文件：

   ```bash
      mkdir -p .cursor/rules
      cp -r /path/to/CursorRIPER/src/.cursor/* .cursor/
      cd .cursor/rules/
      rename 's/\.md$/.mdc/' *.md
   ```

2. **验证安装**

   您的项目现在应该具有以下结构：

   ```
   your-project/
   └── .cursor/
       ├── rules/
       │   ├── core.mdc
       │   ├── state.mdc
       │   ├── start-phase.mdc
       │   ├── riper-workflow.mdc
       │   └── customization.mdc
       └── cursorignore
   ```

## 开始新项目

1. **初始化框架**

   在 Cursor IDE 中打开您的项目，并使用聊天功能初始化框架：

   ```
   /start
   ```

   或

   ```
   BEGIN START PHASE
   ```

2. **遵循 START 阶段**

   框架将引导您完成 START 阶段：

   1. 需求收集 (Requirements Gathering)
   2. 技术选择 (Technology Selection)
   3. 架构定义 (Architecture Definition)
   4. 项目搭建 (Project Scaffolding)
   5. 环境设置 (Environment Setup)
   6. 内存库初始化 (Memory Bank Initialization)

3. **完成内存库设置**

   确保创建并填充所有必需的内存文件：
   
   - `projectbrief.md`
   - `systemPatterns.md`
   - `techContext.md`
   - `activeContext.md`
   - `progress.md`

## 使用 RIPER 工作流

完成 START 阶段后，您将自动过渡到 RIPER 工作流。使用以下命令在不同模式之间切换：

- `/research` 或 `ENTER RESEARCH MODE` - 收集信息并理解现有代码
- `/innovate` 或 `ENTER INNOVATE MODE` - 头脑风暴潜在的方法
- `/plan` 或 `ENTER PLAN MODE` - 创建详细的实施计划
- `/execute` 或 `ENTER EXECUTE MODE` - 实施已批准的计划
- `/review` 或 `ENTER REVIEW MODE` - 根据计划验证实施情况

## 自定义

您可以通过编辑 `.cursor/rules/customization.mdc` 来自定义框架行为。一些关键设置包括：

- 响应详细程度
- 代码风格偏好
- 内存更新频率
- 自定义命令别名

更多详情请参见[自定义指南](customization-guide.md)。

## 故障排除

如果您遇到框架问题：

1. 验证 `.cursor/rules/` 中是否存在所有必需的文件
2. 检查状态不一致
3. 确保内存库文件存在并格式正确
4. 尝试重启 Cursor IDE

如需更多帮助，请参阅[故障排除指南](troubleshooting-guide.md)。

---

*CursorRIPER 框架防止编码灾难，同时在会话之间保持完美连续性。* 