# 公开方法来源

本 Skill 只吸收公开仓库中的通用机制并重新组织，没有复制其完整文本或绑定特定框架。

- `anthropics/skills` 的 `frontend-design`：从具体用户、主题与真实内容出发，形成有明确观点且非模板化的前端视觉方向。https://github.com/anthropics/skills/blob/main/skills/frontend-design/SKILL.md
- `PaulRBerg/agent-skills` 的 `frontend-design`：实现后使用浏览器或截图工具检查窄屏、宽屏、交互状态和视觉缺陷，不用源码检查冒充渲染验证。https://github.com/PaulRBerg/agent-skills/blob/main/skills/frontend-design/SKILL.md
- `anthropics/knowledge-work-plugins` 的 `design-critique`：从可用性、层级、一致性和具体设计证据组织审查，并支持以截图或设计稿作为审查对象。https://github.com/anthropics/knowledge-work-plugins/blob/main/design/skills/design-critique/SKILL.md
- `Digidai/product-manager-skills`：把产品工作组织为战略、发现、优先级、执行与指标，而非功能堆叠。https://github.com/Digidai/product-manager-skills
- `wshobson/agents`：按交付路径组合产品上下文、API、前端、后端、数据库、测试、安全、可观察性与决策记录。https://github.com/wshobson/agents
- `saeed-vayghan/gemini-agent-skills` 的后端开发 Skill：强化 HTTP 语义、数据模型与索引、认证授权、错误处理、日志、性能和安全基线。https://github.com/saeed-vayghan/gemini-agent-skills/blob/master/.gemini/skills/backend-developer/SKILL.md
- 本地 `grill-me` Skill：一次只问一个问题，沿依赖关系逐步解决决策树，并在完成后总结所有决定。
- UI 素材目录优先采用许可证明确、社区关注度高的官方仓库：`shadcn-ui/ui`、`radix-ui/themes`、`radix-ui/primitives`、`mantinedev/mantine`、`tailwindlabs/headlessui`、`saadeghi/daisyui` 与 `lucide-icons/lucide`；具体选择和边界见 `ui-material-libraries.md`。

更新时优先保留可跨技术栈复用、能改变执行行为、可验证的机制；不要因某仓库星数高就照搬其人格、目录或刚性流程。
