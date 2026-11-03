# 配套 Skill：投研适配版

本仓库提供可安装的 [investment-research-wiki](../skills/investment-research-wiki/SKILL.md)。它基于社区 karpathy-llm-wiki 的流程改写，适配本指南的客户库；客户无需另装上游原版。

Skill 是 Codex 可按任务调用的操作说明。它负责入库、查询、检查、审核执行和中断恢复；目录、研究重点、整理深度与权限由客户库的 AGENTS.md、个人配置和规则决定。首次访谈仍从 [START-HERE.md](../START-HERE.md) 开始。

## 已做的适配

| 上游方案 | 本仓库适配版 |
|---|---|
| 固定 raw/wiki 结构 | 读取客户实际路径映射，支持中文目录与自定义分类 |
| 首次入库创建目录 | 先访谈并确认方案，再初始化；日常 Skill 不跳过设置 |
| 直接编写与联动知识页 | 普通事实依权限更新，判断变化、冲突及新页转正走客户审核规则 |
| 同名原件增加文件名后缀 | 按来源与指纹去重；部分完成沿用原 ID、卡片与原件继续读取 |
| 固定文章模板和来源字段 | 使用客户本机模板，保留投研口径、页码、阅读范围和重点深度 |
| 检查时自动修复部分问题 | 检查默认只读，修复遵循明确授权；保护人工内容 |

保留了上游的证据定位、增量分流和相关页检查思路。没有移植依赖 raw/wiki 与 Raw 字段的检查脚本；当前由 Codex 按客户结构执行检查，不声称存在自动事实校验器。

## 安装到客户库

首次设置时，AI 把此 Skill 列入初始化方案，客户确认后按[实施指南](SETUP-AND-ACCEPTANCE.md)安装。只安装到客户库，不安装到全局目录，也不把说明书仓库当作客户库。

从本指南同一版本完整复制 `skills/investment-research-wiki/` 到客户库：

```text
客户知识库/
├── AGENTS.md
└── .agents/
    └── skills/
        └── investment-research-wiki/
            ├── SKILL.md
            ├── NOTICE.md
            └── LICENSE
```

保留三个文件及原目录关系。`.agents` 是以点开头的真实文件夹名，不能误建成 `agents`。复制后回读文件，核对客户根 AGENTS.md 的 Skill 链接及 Skill 所需的本机规则入口。客户目录改名不需要改 Skill 内部路径，因为它从客户根入口查找规则。

对已有客户库：先读取现有 AGENTS.md、个人配置和交接，展示新增文件与入口改动；取得该范围授权后安装，保留原规则和自定义。同名 Skill 已存在时先比较，确认升级差异后更新，不覆盖其他技能。若已安装上游 karpathy-llm-wiki，说明两者冲突并由客户确认停用方式，不自动删除。

## 使用与验收

让客户在 Codex 中打开客户知识库目录并开始新对话。可发送：

> 请使用 $investment-research-wiki，先读取本库规则和交接，说明当前待办，再按我的配置整理这份材料。判断变化给我审核。

也可直接说“只根据库内资料回答……”或“检查知识库的一致性，先不要修改”。若当前 Codex 未自动发现 Skill，先检查工作目录与安装文件，再让它直接读取本机 `.agents/skills/investment-research-wiki/SKILL.md`；不需要为了继续任务改全局配置。

分别记录“文件已安装”“新对话发现或显式读取”“样例流程通过”。不能仅凭复制成功就声称 Skill 已被发现或实际整理通过。验收包含自定义路径查找、带出处查询、重复/部分材料恢复和冲突审核；真实材料与 Windows 环境按客户实际结果记录。

## 来源与许可

上游为 [Astro-Han/karpathy-llm-wiki](https://github.com/Astro-Han/karpathy-llm-wiki/tree/eafcc77001e496cc43499e4923b663aec722c813)，锁定提交 `eafcc77001e496cc43499e4923b663aec722c813`。本适配版已改名，具体改动见 [NOTICE](../skills/investment-research-wiki/NOTICE.md)，保留 [MIT 许可](../skills/investment-research-wiki/LICENSE)。它不是 Karpathy 或 OpenAI 官方产品。
