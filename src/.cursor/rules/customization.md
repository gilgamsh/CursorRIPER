---
description: "CursorRIPER框架 - 自定义"
globs: 
alwaysApply: true
version: "1.0.2"
date_created: "2025-04-05"
last_updated: "2025-04-06"
framework_component: "customization"
priority: "medium"
scope: "optional"
---
<!-- 注意：Cursor会去掉其他所有头部信息，只保留前三项。 -->
# CursorRIPER框架 - 自定义
# 版本 1.0.2

## AI处理指令
此文件包含CursorRIPER框架的用户定义自定义设置。作为AI助手，你必须：
- 在核心框架组件之后加载此文件（如果存在）
- 应用这些自定义设置以覆盖默认框架行为
- 除非用户明确要求，否则绝不修改此文件
- 在每个会话的第一个回复中确认活跃的自定义设置

## 用户偏好

### 响应风格
RESPONSE_VERBOSITY: "BALANCED"
# 可能的值："CONCISE"（简洁）, "BALANCED"（平衡）, "DETAILED"（详细）
# 控制AI响应中的细节级别

CODE_STYLE_PREFERENCES: ""
# 指定代码风格偏好（缩进、命名约定等）

EXPLANATION_LEVEL: "MEDIUM"
# 可能的值："MINIMAL"（最小）, "MEDIUM"（中等）, "COMPREHENSIVE"（全面）
# 控制代码提供的解释程度

### 模式行为
SUGGEST_MODE_TRANSITIONS: true
# 如果为true，AI可以在适当时建议模式转换

AUTO_MODE_TRANSITION: false
# 如果为true，AI可以在模式之间自动转换（除了转到EXECUTE）
# EXECUTE模式始终需要明确的用户授权

PLAN_QUESTION_COUNT: 5
# 在PLAN模式下要问的澄清问题数量

### 记忆管理
AUTO_UPDATE_MEMORY: true
# 如果为true，AI会在重大变更后自动更新记忆文件

MEMORY_UPDATE_FREQUENCY: "AFTER_COMPLETION"
# 可能的值："AFTER_EVERY_RESPONSE"（每次响应后）, "AFTER_COMPLETION"（完成后）, "MANUAL_ONLY"（仅手动）
# 控制何时更新记忆文件

REQUIRED_MEMORY_FILES: ["projectbrief.md", "activeContext.md", "progress.md"]
# 框架正常运作所必需的记忆文件列表

### 归档行为
AUTO_ARCHIVE_START_PHASE: true
# 如果为true，START阶段将在完成后自动归档

BACKUP_FREQUENCY: "DAILY"
# 可能的值："NEVER"（从不）, "DAILY"（每日）, "WEEKLY"（每周）, "BEFORE_CHANGES"（变更前）
# 控制记忆库备份的频率

KEEP_BACKUP_COUNT: 5
# 删除最旧备份前保留的备份集数量

## @符号自定义

### 符号使用偏好
AUTO_SUGGEST_SYMBOLS: true
# 如果为true，AI会在适当时建议相关@符号

SYMBOL_SUGGESTION_FREQUENCY: "MEDIUM"
# 可能的值："LOW"（低）, "MEDIUM"（中）, "HIGH"（高）
# 控制提供@符号建议的频率

MAINTAIN_SYMBOL_REGISTRY: true
# 如果为true，AI会自动更新@符号注册表

### 符号上下文偏好
DEFAULT_SYMBOL_DEPTH: "FILE"
# 可能的值："FILE"（文件）, "DIRECTORY"（目录）, "REPOSITORY"（仓库）
# 控制@符号的默认上下文深度

CODE_SYMBOL_PREFERENCE: "FUNCTION"
# 可能的值："FUNCTION"（函数）, "CLASS"（类）, "VARIABLE"（变量）, "ALL"（全部）
# 控制在建议中优先考虑哪些代码符号

### 符号模板别名
SYMBOL_ALIASES: {
  "@f:": "@Files:",
  "@d:": "@Folders:",
  "@c:": "@Code:",
  "@doc:": "@Docs:",
  "@w:": "@Web:",
  "@g:": "@Git:"
}
# @符号的自定义短别名

## 高级自定义

### 命令别名
CUSTOM_COMMANDS: {
  "/r": "/research",
  "/i": "/innovate",
  "/p": "/plan",
  "/e": "/execute",
  "/rv": "/review"
}
# 模式转换的自定义命令快捷方式

### 模式扩展
RESEARCH_MODE_EXTENSIONS: []
# RESEARCH模式的附加行为

INNOVATE_MODE_EXTENSIONS: []
# INNOVATE模式的附加行为

PLAN_MODE_EXTENSIONS: []
# PLAN模式的附加行为

EXECUTE_MODE_EXTENSIONS: []
# EXECUTE模式的附加行为

REVIEW_MODE_EXTENSIONS: []
# REVIEW模式的附加行为

### 框架扩展
CUSTOM_PHASES: []
# 标准阶段以外的附加项目阶段

CUSTOM_WORKFLOWS: []
# 特定项目类型的自定义工作流

## 用户文档偏好

### 文档格式
DOCUMENTATION_STYLE: "MARKDOWN"
# 生成文档的格式

INCLUDE_CODE_COMMENTS: true
# 是否在生成的代码中包含详细注释

CODE_BLOCK_LANGUAGE_TAGS: true
# 代码块中是否包含语言标签

### AI输出格式
MODE_DECLARATION_FORMAT: "[MODE: {mode}]"
# 模式声明的格式字符串

PROGRESS_INDICATOR_FORMAT: "[{current_step}/{total_steps}]"
# 响应中进度指示器的格式

## 自定义项目结构

PROJECT_TYPE: "DEFAULT"
# 识别项目类型以进行专门处理

CUSTOM_FOLDER_STRUCTURE: {}
# 项目脚手架的自定义文件夹结构定义

TECHNOLOGY_PRESETS: {}
# 预定义的技术栈，用于快速选择

---

*此文件包含CursorRIPER框架的用户定义自定义设置。编辑这些设置以根据您的偏好调整框架行为。* 