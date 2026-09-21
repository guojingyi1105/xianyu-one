# 咸鱼一号（Xianyu One）

一个面向应用开发的开放式 Agent Skill：把模糊想法或业务需求转化为合适、易用、结构清晰、可验证、可上线的产品。

它会根据任务按需调度：

- 深度访谈与需求澄清
- 产品契约、范围和验收设计
- 软件架构选择、模块边界与依赖治理
- AI Coding 仓库地图、分层指令、变更预算与验证闭环
- 用户主导的前端设计
- 开源 UI 素材库选择
- 桌面端与移动端真实渲染审查
- 前后端、数据库、权限和第三方集成
- 测试、系统调试、发布门禁与复盘
- 基于仓库地图、按需读取和分层验证的 token 节约执行

特别适合不会写 PRD、不熟悉技术栈，但希望参与产品决策和界面审查的用户。

## 安装

仓库中的 `xianyu-one/` 是完整 Skill 目录。

### Codex

将 `xianyu-one` 目录复制到个人 Skills 目录：

```text
~/.codex/skills/xianyu-one/
```

### WorkBuddy

将 `xianyu-one` 目录压缩为 ZIP，确保 ZIP 根目录直接包含 `SKILL.md`，然后在“技能 → 添加技能 → 上传技能”中安装。

### 其他 Agent Skills 客户端

将完整的 `xianyu-one` 目录放入该客户端的 Skills 目录。必须同时保留 `SKILL.md`、`references/` 和可选的 `agents/`。

## 使用示例

```text
使用 $xianyu-one 帮我把这个想法梳理清楚，并开发成可以测试的产品。
```

```text
使用咸鱼一号逐步问我，让我参与设计前端，并生成桌面和移动端渲染图供我审查。
```

```text
使用咸鱼一号检查这个应用是否已经达到上线条件。
```

```text
使用咸鱼一号评估并优化这个项目的软件架构，建立让 AI Coding 不会乱改代码的仓库规范。
```

## 设计理念

- 从真实用户任务出发，不从页面或技术栈出发。
- 区分原型、Demo、测试版和生产版。
- 一次只解决一个关键决策，避免给小白倾倒术语。
- 选择最简单且足够的架构。
- 用可执行边界、规格和验证约束 AI Coding，而不是只提供模糊提示词。
- 使用真实运行、测试和渲染证据，而不是完成声明。
- 保留用户选择、原始业务事实和风险边界。
- 主 Skill 只保留路由与不可省略规则，专业细节按任务从 `references/` 加载。

## Token 节约机制

咸鱼一号不会默认通读整个仓库或机械生成全套文档。它先读取仓库规则、目录/搜索结果和目标文件，再沿调用关系按需展开；验证也从定向检查开始，仅在影响半径或发布风险要求时扩展。该机制借鉴 Aider repo map、Repomix、AGENTS.md、GitHub Spec Kit 与 Agent Skills 渐进加载，并在 `references/token-efficient-execution.md` 中记录依据和边界。

公开方法来源、许可证边界与取舍记录见 [`docs/research-basis.md`](docs/research-basis.md)。该维护资料放在 Skill 运行目录之外，避免增加按需支撑文件预算。

## 开源 UI 素材

Skill 内置经过筛选的素材目录和场景路由，包括 shadcn/ui、Radix、Mantine、Headless UI、daisyUI 和 Lucide。第三方项目仍适用各自许可证；使用前请核对其当前版本与许可条款。

## 许可证

咸鱼一号本身采用 [MIT License](LICENSE)。`references/` 中提到的第三方项目不随本仓库重新授权，仍由各自许可证管理。
