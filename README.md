# x-thinking-skill

一对帮你 **把模糊、混乱的想法逐步想清楚** 的 Claude Code / Codex Skill。
它是你的 **认知合伙人、逻辑编辑和模型挑战者**：先判断你卡在表达、结构、因果、求证还是行动依据，再主动重构表达、补足认知缺口，与你共同沉淀一张可复利的 Obsidian 原子知识卡。

> 设计原则一句话：**共同思考，不做采访器，也不做代写者。** AI 先贡献结构和候选，用户保留经验、价值与最终判断。

## 两个入口

| 命令 | 用途 |
|---|---|
| `/thinking` | 澄清**当下一个**模糊念头 |
| `/thought` | 消化**过去攒下的一堆**碎片笔记（先聚类找主题与矛盾，再挑一个想清） |

也支持直接说「帮我澄清一个想法」「消化一下我过去的笔记」。

## 它怎么工作

**核心约束**：每轮必须产生认知增量 · 先定位卡点再选工具 · 先贡献再提问 · 区分用户原意与 AI 补充 · 区分表达流畅与证据成立 · 不伪造确定性。

**澄清循环**：先路由（定位主要卡点与认知动作）→ 收（接住原料）→ 架（重建层级/因果/反馈）→ 诊（找概念与逻辑问题）→ 补（补概念、机制、变量、证据或替代解释）→ 辩（检查反面与边界）→ 炼（交付当前清晰版本）→ 迁（提炼可复用知识）→ 卡（保存）。

**产物**：一张能快速回忆、也能直接作为口播或文章大纲的 Obsidian 原子卡。核心正文固定为“一句话—问题—解决方案—逻辑—最小闭环”，用自然、具体的话说清原始想法；随后完成用户与角度分析，用一张两列表格并排呈现“用户可能关心的问题”和“共鸣选题句”。选题句用一句有标题感的话戳出用户矛盾和新判断，但不等于最终发布标题。钩子、相似模型等只在明确需要时加入，避免字段重复。

## 安装

把两个 skill 文件夹复制进你的 Claude skills 目录：

```bash
# macOS / Linux
cp -r skills/thinking skills/thought ~/.claude/skills/

# Windows (Git Bash)
cp -r skills/thinking skills/thought ~/.claude/skills/
```

只有真正保存卡片时才检查配置，不在对话开始前打断思考。首次保存会引导设置 Obsidian vault 与卡片文件夹，存到 Claude Code 与 Codex 共用的 `~/.thinking-skill/config.json`；已有的 `~/.claude/thinking-config.json` 会继续兼容。

## 隐私

**你的个人数据不会进入本仓库。** vault 路径等配置只存在本地的 `~/.thinking-skill/config.json`（或兼容的旧配置文件），位于 skill 文件夹之外；你的思考卡片进的是你自己的 Obsidian 库。仓库里只有「方法」，没有「数据」。

## 理论依据

每一步都有出处，完整写在 [`skills/thinking/PRINCIPLES.md`](skills/thinking/PRINCIPLES.md)。脊柱是三个母理论：

- **认知负荷理论 + 工作记忆极限**（Sweller / Cowan）——为什么要外化并分阶段重建结构；
- **写作认知模型**（Hayes–Flower 1981）——为什么同时生成、组织和审阅会卡住；
- **分布式认知 + 元认知**（Clark & Chalmers / Flavell）。

产物形态（可复利原子卡）取自 **Zettelkasten / 常青笔记** 谱系（Luhmann / Ahrens / Matuschak）。

## License

MIT
