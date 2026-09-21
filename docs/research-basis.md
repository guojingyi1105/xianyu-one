# 公开方法来源与取舍记录

本文件用于维护和审计，不属于运行时 Skill 包。咸鱼一号只吸收公开仓库中的通用机制并重新组织，没有复制其完整文本或绑定特定框架。

- `anthropics/skills` 的 `frontend-design`：从具体用户、主题与真实内容出发，形成有明确观点且非模板化的前端视觉方向。https://github.com/anthropics/skills/blob/main/skills/frontend-design/SKILL.md
- `PaulRBerg/agent-skills` 的 `frontend-design`：实现后使用浏览器或截图工具检查窄屏、宽屏、交互状态和视觉缺陷，不用源码检查冒充渲染验证。https://github.com/PaulRBerg/agent-skills/blob/main/skills/frontend-design/SKILL.md
- `anthropics/knowledge-work-plugins` 的 `design-critique`：从可用性、层级、一致性和具体设计证据组织审查，并支持以截图或设计稿作为审查对象。https://github.com/anthropics/knowledge-work-plugins/blob/main/design/skills/design-critique/SKILL.md
- `Digidai/product-manager-skills`：把产品工作组织为战略、发现、优先级、执行与指标，而非功能堆叠。https://github.com/Digidai/product-manager-skills
- `wshobson/agents`：按交付路径组合产品上下文、API、前端、后端、数据库、测试、安全、可观察性与决策记录。https://github.com/wshobson/agents
- `saeed-vayghan/gemini-agent-skills` 的后端开发 Skill：强化 HTTP 语义、数据模型与索引、认证授权、错误处理、日志、性能和安全基线。https://github.com/saeed-vayghan/gemini-agent-skills/blob/master/.gemini/skills/backend-developer/SKILL.md
- 本地 `grill-me` Skill：一次只问一个问题，沿依赖关系逐步解决决策树，并在完成后总结所有决定。
- UI 素材目录优先采用许可证明确、社区关注度高的官方仓库：`shadcn-ui/ui`、`radix-ui/themes`、`radix-ui/primitives`、`mantinedev/mantine`、`tailwindlabs/headlessui`、`saadeghi/daisyui` 与 `lucide-icons/lucide`；具体选择和边界见 `ui-material-libraries.md`。
- 架构与 AI Coding 采用 `github/spec-kit`、`agentsmd/agents.md`、`nrwl/nx`、`vercel/turborepo`、`alan2207/bulletproof-react`、`architecture-decision-record/architecture-decision-record` 与 `github/awesome-copilot` 中可跨技术栈复用的机制；具体取舍见 `architecture-and-ai-coding.md`。
- Token 与上下文优化采用以下公开实现，并在 `token-efficient-execution.md` 中记录取舍：
  - `Aider-AI/aider` repo map：在活动 token 预算内选择关键符号和与当前任务相关的依赖图内容。https://github.com/Aider-AI/aider/blob/main/aider/website/docs/repomap.md
  - `yamadashy/repomix`：使用 include/ignore、token-count tree、Tree-sitter 压缩和安全检查控制送入模型的仓库内容。https://github.com/yamadashy/repomix
  - `agentsmd/agents.md`：目录层级限定指令作用域，子目录只补充或覆盖局部规则，避免重复全局指令。https://github.com/agentsmd/agents.md
  - `github/spec-kit`：保留核心交付流程，仅在存在实质歧义时增加 clarify/checklist/analyze，并避免先为整个旧系统补文档。https://github.com/github/spec-kit
  - `anthropics/skills` 的 `skill-creator`：元数据、主 Skill 与按需资源三级渐进加载，脚本用于确定性重复任务。该仓库声明为 source-available，故这里只借鉴机制，不把其内容作为本项目 MIT 授权的一部分。https://github.com/anthropics/skills/blob/main/skills/skill-creator/SKILL.md

更新时优先保留可跨技术栈复用、能改变执行行为、可验证的机制；不要因某仓库星数高就照搬其人格、目录或刚性流程。
