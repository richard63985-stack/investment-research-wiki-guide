# 投研 Wiki 与万得 API：给 Codex 的设置指南

版本：0.1.5｜整理日期：2026-11-03

为使用 Windows 和 Codex 的投研人员建立自己的研究知识库。先了解研究需求，再确认架构和整理规则，最后设置并用一份材料试运行。万得 API 可以独立接入，不是使用 Wiki 的前提。

## 把这个仓库交给 Codex

复制下面的话，发送给客户的 Codex：

> 请阅读 https://github.com/richard63985-stack/investment-research-wiki-guide 的 README.md 和 START-HERE.md，帮助我设置投研 Wiki。先向我说明它的用途，再通过分轮提问了解我的研究工作，给出有推荐意见的架构与整理规则，得到我确认后再初始化。先用一份材料校准，不要直接批量处理。若我要求接入万得，按仓库的万得教程检查接口类型和环境，再验证连接与取数。

也可让 AI 读取 [纯文本入口](https://raw.githubusercontent.com/richard63985-stack/investment-research-wiki-guide/main/START-HERE.md)。如果 Codex 无法读取链接，下载 [仓库 ZIP](https://github.com/richard63985-stack/investment-research-wiki-guide/archive/refs/heads/main.zip) 并解压，让 Codex 打开解压目录，发送“请阅读 START-HERE.md，开始引导我设置投研 Wiki”。这里是说明书目录，客户知识库另选一个本机目录。客户不需要会 Git，也不需要安装 grilling 技能。

## 会得到什么

- 根据你的覆盖对象定制的公司、行业、研究框架等知识页面。
- 原始资料、材料卡片与综合知识之间可追溯的关联。
- 明确的整理重点、速览/标准/深度三级规则和更新权限。
- 可持续使用的本机 AI 操作入口、个人配置与交接记录。
- 可选：万得连接验证、最小取数样例及日常取数规范。

Markdown 是普通文本文件；Codex 维护这些文件，Obsidian 可作为可选阅读工具。首版不要求安装额外 Wiki 插件、数据库或服务器。

## 内容导航

| 内容 | 入口 |
|---|---|
| AI 执行流程 | [从这里开始](START-HERE.md) |
| 需求访谈 | [分轮访谈](wiki/INTERVIEW.md) |
| 默认架构 | [目录与页面职责](wiki/ARCHITECTURE.md) |
| 整理标准与权限 | [整理规则](wiki/PROCESSING.md) |
| 初始化、日常使用和验收 | [实施指南](wiki/SETUP-AND-ACCEPTANCE.md) |
| 日常整理与中断恢复 | [操作流程](wiki/OPERATIONS.md) |
| 页面模板 | [模板目录说明](templates/README.md) |
| 虚构材料试整理示例 | [样例](examples/CALIBRATION.md) |
| 万得接入 | [Windows 接入教程](wind/SETUP.md) |
| 万得日常使用 | [取数与落库规则](wind/USAGE.md) |
| 来源、维护与验证范围 | [来源](SOURCES.md) · [维护说明](MAINTAINERS.md) · [检查记录](VALIDATION.md) |

本仓库只分发通用规则和虚构示例。客户的材料、账号、个人配置和取数结果留在独立本机知识库中。使用云端 AI 处理资料仍需符合客户自己的资料使用权限；本地保存不等于离线模型处理。

这是独立编写的实施指南，不是 Karpathy、OpenAI 或万得官方产品。官方资料与本指南设计建议的边界见来源文件。Windows 实机与客户账户验收尚未完成。
