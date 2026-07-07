# x-thinking-skill

一对帮你 **把模糊、混乱的想法逐步想清楚** 的 Claude Code / Claude Agent Skill。
它不替你思考，只当 **一面会追问的镜子**——用「一次只问一个问题」的多轮对话，把念头澄清，最终沉淀成一张 **可复利的原子知识卡**（写进你的 Obsidian）。

> 设计原则一句话：**镜子，不是作者。** 绝不替你造观点、写结论——否则它就退化成又一个「帮你写」的 AI。

## 两个入口

| 命令 | 用途 |
|---|---|
| `/thinking` | 澄清**当下一个**模糊念头 |
| `/thought` | 消化**过去攒下的一堆**碎片笔记（先聚类找主题与矛盾，再挑一个想清） |

也支持直接说「帮我澄清一个想法」「消化一下我过去的笔记」。

## 它怎么工作

**四条铁律**：镜子不是作者 · 一次只问一个问题 · 用你自己的话反馈 · 多轮慢逼近。

**澄清循环**：倒（无评判倒出）→ 镜（用你的话复述）→ 锚（钻到真问题，用 5-Why 别停在表面）→ 凿（四把凿子：定义／例子／前提／反面，一次一把）→ 分（拆开搅在一起的层）→ 炼（逼出一句话主张＝卡片标题）→ 卡（逼出最小可行方案：一句话／流程／SOP）。

**产物**：一张 Obsidian 原子卡——声明式标题（你的主张）／一个核心问题／最小可行方案／思考留痕（背景＋思考过程），可选在底部追加 3–5 条**单向**关联。

## 安装

把两个 skill 文件夹复制进你的 Claude skills 目录：

```bash
# macOS / Linux
cp -r skills/thinking skills/thought ~/.claude/skills/

# Windows (Git Bash)
cp -r skills/thinking skills/thought ~/.claude/skills/
```

首次运行 `/thinking` 时会引导你设置 Obsidian vault 路径与卡片文件夹，存到 `~/.claude/thinking-config.json`。

## 隐私

**你的个人数据不会进入本仓库。** vault 路径等配置只存在本地的 `~/.claude/thinking-config.json`（在 skill 文件夹之外，且被 `.gitignore` 忽略）；你的思考卡片进的是你自己的 Obsidian 库。仓库里只有「方法」，没有「数据」。

## 理论依据

每一步都有出处，完整写在 [`skills/thinking/PRINCIPLES.md`](skills/thinking/PRINCIPLES.md)。脊柱是三个母理论：

- **认知负荷理论 + 工作记忆极限**（Sweller / Miller / Cowan）——「一次一问」的根据；
- **写作认知模型**（Hayes–Flower 1981）——为什么「边写边想」很慢，以及本 skill 如何把「质疑者」角色外包出去；
- **分布式认知 + 元认知**（Clark & Chalmers / Flavell）。

产物形态（可复利原子卡）取自 **Zettelkasten / 常青笔记** 谱系（Luhmann / Ahrens / Matuschak）。

## License

MIT
