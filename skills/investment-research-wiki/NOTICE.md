# 来源与适配

适配版本：0.1.8（2026-11-03）。

本 Skill 基于 [Astro-Han/karpathy-llm-wiki](https://github.com/Astro-Han/karpathy-llm-wiki/tree/eafcc77001e496cc43499e4923b663aec722c813) 的 SKILL.md 入库、查询与检查工作流改写。上游版权为 Copyright (c) 2026 Yuhan Lei，MIT 许可原文保留在同目录 [LICENSE](LICENSE)。这是投研指南项目的适配版本，不是上游原版，也不是 Karpathy 或 OpenAI 官方产品。

适配后的行为：

- 固定 raw/wiki 结构改为客户 AGENTS.md、个人配置路径映射及系统索引。
- 首次入库自动初始化改为先完成投研访谈与方案确认，Skill 用于已设置客户库的日常执行。
- 使用客户本机模板与整理规则，不复制上游固定字段模板。
- 保留来源核对、增量分流和关联页检查，加入投研深度、判断审核、人工内容保护、来源去重与部分阅读恢复。
- 查询及单独检查默认只读；保存答案按客户权限更新或生成候选，不强制新建正式归档页。
- 不分发上游 scripts/check_evidence.py；其目录/字段假设不适用于定制库。检查由 AI 按实际结构执行，未提供等价自动检查脚本。

许可证适用于上游许可材料；本说明不为整个投研指南仓库新增开源许可。安装或分发本适配目录时保留本说明与 LICENSE。
