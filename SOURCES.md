# 来源与证据边界

核对日期：2026-11-03。引用均链接原始来源，具体客户环境仍需现场验证。

| 来源 | 用途 | 边界 |
|---|---|---|
| [Karpathy LLM Wiki idea file](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f) | 原始材料与持续维护 Wiki 的概念来源 | 本仓库的投研目录与规则为定制设计，不是其官方实现 |
| [Astro-Han/karpathy-llm-wiki](https://github.com/Astro-Han/karpathy-llm-wiki/tree/eafcc77001e496cc43499e4923b663aec722c813) | 可选社区 Skill 及安装方式 | 非官方实现；目录与审核规则尚未适配本投研库，见[兼容性说明](wiki/OPTIONAL-SKILLS.md) |
| [Wind Client API 官网](https://www.wind.com.cn/portal/zh/ClientApi/index.html) | 支持平台/语言、CG 代码生成器 | 产品介绍，不是完整 Python 安装手册 |
| [Wind 下载中心](https://www.wind.com.cn/download.htm) | 当前官方安装包和手册入口 | 执行时重新查看，不能固定旧下载地址 |
| [Windows 安装配置手册](https://www.wind.com.cn/windftp/wind.net/WFT_Windows_Configuration_Manual.pdf) | 终端安装、目录选择、登录和网络配置 | PDF 封面为 2024.12；下载页标注日期与封面不同，采用文档自身标注。旧最低版本不代表今日推荐；不复制旧网络清单 |
| [WindQuant/Official](https://github.com/WindQuant/Official) 与 [历史 Python 包装源码](https://github.com/WindQuant/Official/blob/master/WAPIWrapper/WAPIWrapperPython/WindPy.py) | 交叉核对基本连接函数 | 历史来源，不用于下载安装或证明当前 Python 兼容性 |
| [writing-for-agents 上游](https://github.com/mattpocock/skills) | 分层指令、按任务读取和完成条件的方法参考 | 本文档独立编写，未分发该技能全文 |

访谈方法参考维护者已安装的 grilling 技能：按决策依赖分轮、每题提供建议、追问矛盾、确认共同理解后执行。客户无需安装该技能；本仓库不分发其原文件，也不推测未核实的上游来源或许可。

投研预设从维护者既有 Wiki 的结构与使用经验抽象而来，未复制私有材料、观点、账户或设备配置。

万得 Python 插件的最新具体安装步骤、支持的解释器版本、字段与权限，须以客户当前终端官方帮助/CG 核实。无法访问相应帮助时记录阻塞，不能把第三方文章替代为官网指南。公开资料已支持的部分与本指南建议的执行流程在万得教程中分别注明。
