# ai-berkshire-hermes-runtime

- 先进入 `~/work/hermes-agent/skills/ai-berkshire`。
- Claude Code / Codex 工具名按 Hermes 能力映射：`Bash` 用 `terminal`，`Read/Write/Edit` 用文件工具，`WebSearch/WebFetch` 用 Hermes 可用搜索/抓取工具。
- 上游 `TeamCreate`、`TaskCreate`、`TaskUpdate`、`SendMessage`、`TeamDelete` 视为团队流程语义，不要求调用同名 API。
- 需要子 agent 时，使用 Hermes `delegate_task` 的 single 模式逐个执行；禁止使用 `tasks=[...]` batch 并行模式。多个角色按原 skill 顺序一个一个跑。
- 不需要子 agent 的步骤，在当前 Hermes 会话中按原顺序执行。
- 需要提交产物时，创建分支并开 PR，不直接提交或推送 `main`；创建 PR 后，先返回 PR 链接，再按 preview 流程返回预览链接。
