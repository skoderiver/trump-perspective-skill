# trump-perspective-skill

把 [yangbuyiya/trump-perspective-skill](https://github.com/yangbuyiya/trump-perspective-skill) 适配为本地可用的 Codex 插件仓库。

这个仓库保留了上游 Skill 的核心内容和 research 资料，并补齐了 Codex 需要的插件清单、marketplace 入口和 `agents/openai.yaml`。

这不是政治背书，也不是价值认同。
它是一个基于公开资料构建的视角分析、行为预判与风格模拟工具。

## 仓库内容

- `plugins/trump-perspective-skill/.codex-plugin/plugin.json`
  Codex 插件清单。
- `plugins/trump-perspective-skill/skills/trump-perspective-skill/SKILL.md`
  实际触发的技能定义。
- `plugins/trump-perspective-skill/skills/trump-perspective-skill/references/research/`
  上游导入的研究资料。
- `.agents/plugins/marketplace.json`
  当前仓库内的本地 marketplace 入口。

## 在 Codex 中使用

如果你直接用 Codex 打开这个仓库，插件入口已经就位：

1. 打开本仓库根目录。
2. Codex 会从 `.agents/plugins/marketplace.json` 发现本地插件。
3. 插件名是 `trump-perspective-skill`，技能名也是 `trump-perspective-skill`。

常见触发方式：

- `用特朗普视角分析当前中东局势`
- `预测特朗普接下来会怎么对待伊朗问题`
- `切换到特朗普口吻，和我聊一轮关税战`
- `Use $trump-perspective-skill to analyze this issue from the Trump perspective.`

## 目录结构

```text
.
├─ .agents/
│  └─ plugins/marketplace.json
└─ plugins/
   └─ trump-perspective-skill/
      ├─ .codex-plugin/plugin.json
      ├─ LICENSE
      └─ skills/
         └─ trump-perspective-skill/
            ├─ SKILL.md
            ├─ agents/openai.yaml
            └─ references/research/
```

## 来源说明

- 上游项目: [yangbuyiya/trump-perspective-skill](https://github.com/yangbuyiya/trump-perspective-skill)
- 上游许可证: MIT

这个仓库主要做了三件事：

1. 生成 Codex 可识别的插件骨架。
2. 导入上游 `SKILL.md` 和 research 资料。
3. 补齐 `plugin.json`、`marketplace.json` 和 `agents/openai.yaml`。

## 当前状态

- 已通过技能校验脚本 `quick_validate.py`
- 已包含本地 marketplace 配置
- 已推送到 GitHub 默认分支 `main`
