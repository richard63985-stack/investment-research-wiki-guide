# 可选的 LLM Wiki Skill

Skill 是供 AI 按需读取的一组操作说明。使用本投研指南不需要额外安装 Skill；初始化、查询和整理流程已经包含在本仓库及生成的客户库规则中。

## 找到的社区方案

[Astro-Han/karpathy-llm-wiki](https://github.com/Astro-Han/karpathy-llm-wiki) 将 Karpathy 的 LLM Wiki 概念做成可安装的 Skill，提供资料入库、知识查询和质量检查，声明支持 Codex。它是社区实现，不是 Karpathy 或 OpenAI 官方产品。

- [已核对版本](https://github.com/Astro-Han/karpathy-llm-wiki/tree/eafcc77001e496cc43499e4923b663aec722c813)：`eafcc77001e496cc43499e4923b663aec722c813`，核对日期 2026-11-03。
- [Skill 原文](https://github.com/Astro-Han/karpathy-llm-wiki/blob/eafcc77001e496cc43499e4923b663aec722c813/SKILL.md)。
- [安装说明](https://github.com/Astro-Han/karpathy-llm-wiki/blob/eafcc77001e496cc43499e4923b663aec722c813/README.md)。
- [MIT 许可证](https://github.com/Astro-Han/karpathy-llm-wiki/blob/eafcc77001e496cc43499e4923b663aec722c813/LICENSE)，版权归 Yuhan Lei。本仓库提供入口与兼容性说明，未复制或改写上游 Skill。

## 对投研客户的建议

**已经按本指南建立投研库：继续使用客户库的 AGENTS.md 和个人配置，不直接启用这份上游 Skill。** 两套规则的关键差异如下：

| 项目 | 上游 Skill 默认行为 | 本投研指南 |
|---|---|---|
| 目录 | 固定 `raw/`、`wiki/`，知识页只允许一层主题子目录 | 访谈后确定目录，允许客户映射与调整 |
| 知识页权限 | AI 直接编写和联动更新页面 | 保护人工内容，判断变化、冲突和新页面转正进入审核 |
| 来源去重 | 同名原始文件添加数字后缀 | 先查材料登记、来源与处理进度，支持分次读取同一材料 |
| 检查 | 可自动修索引、链接；脚本按上游目录和字段检查 | 遵守客户的写入权限与实际目录，引用保留材料定位和阅读范围 |

不能只在安装时加一句“以客户规则为准”就认为适配完成；上游的模板和检查脚本也依赖它自己的结构。不要把现有投研库重命名成 `raw/wiki` 来迁就 Skill，也不要把“部分阅读”变成重复入库。

如果将来要在投研库中正式使用，先单独适配 Skill、模板和脚本，再用客户库副本验证目录、权限、引用、续读和去重；通过后才替换日常入口。当前没有完成这项适配。

## 想单独体验上游 Skill

适合尚未建立知识库、愿意采用上游通用结构的人。请另选一个空白体验目录，与投研库分开。

可以把下面的话发给 Codex：

> 请在我指定的独立空白体验目录中，安装并试用 Astro-Han/karpathy-llm-wiki，使用提交 eafcc77001e496cc43499e4923b663aec722c813。先读取该版本 README.md、SKILL.md 和 LICENSE，核对目标目录；只安装到体验目录的 .agents/skills/karpathy-llm-wiki/，保留 SKILL.md、references/、scripts/ 及 LICENSE 的目录关系。不要安装到全局目录。如果目标已有同名 Skill 或不是空白体验目录，先报告现状，不覆盖。安装后列出实际文件，提示我在 Codex 中打开体验目录并开始新对话；用一份无敏感信息的样例验证资料入库、带出处查询和检查。不要改动我的正式投研库。

安装时，Codex 应从锁定版本获取文件并检查完整性；只复制一个 SKILL.md 会缺少它引用的模板和检查脚本。运行脚本前先检查其内容及依赖；Windows 上使用实际可用的 Python 命令，不能直接假设存在 `python3`。不能联网或缺少运行环境时，明确报告未完成步骤。

新对话可先发送：“请使用 karpathy-llm-wiki，说明当前知识库位置和操作规则，先不要入库。”确认识别的是体验目录后，再提供样例。

本仓库只核对了上游说明、规则和许可证，未在客户 Windows 上安装或运行该 Skill。上游的检查结果不等于投研事实已核实，也不替代人工判断与来源复核。
