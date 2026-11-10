# Paper Reading 辅助程序说明

本文说明基于 Norman Paper Reading 的本地 PDF 辅助程序。定制技能的安装、HTML 输出和语料库用法见[仓库说明](../README.md)，具体行为遵循本目录的 [SKILL.md](SKILL.md)。

## 技能用途 / Purpose

Norman Paper Reading 用于阅读指定科研论文，梳理研究问题、设计、证据、图表、公式和后续研究方向。
Norman Paper Reading reads a specified research paper and explains its question, design, evidence, figures, equations, and possible next steps.

它可以做快速概述、完整精读、面向复现的延伸分析，也可以只解释一张图、一条公式或一段文字。
It can produce a quick overview, a full close reading, a reproduction-oriented analysis, or an explanation of one figure, equation, or passage.

## 在 Codex 中使用 / Use in Codex

上传论文 PDF 或提供论文链接，并在请求中写出技能名和希望的阅读深度。
Upload the paper PDF or provide a paper link, and name the skill and desired reading depth in your request.

例如，输入“使用 `$paper-reading` 精读这篇论文，重点解释图 2 和研究设计”。
For example, ask “Use `$paper-reading` for a close reading of this paper, focusing on Figure 2 and the study design.”

| 阅读方式 / Mode | 适用请求 / When to use | 主要内容 / Main content |
| --- | --- | --- |
| 快速总结 / Quick | 想抓住研究问题、方法、主要结果和阅读价值。 / You want the question, method, main results, and reading value. | 核心设计、关键结果和阅读重点。 / Core design, key results, and reading priorities. |
| 完整精读 / Deep | 想理解论文全貌及关键实验、方法或理论。 / You want the full paper and its key experiments, methods, or theory. | 研究故事、图表、公式和证据边界。 / Research storyline, figures, equations, and evidence boundaries. |
| 延伸分析 / Extend | 想把论文用于自己的课题。 / You want to apply the paper to your project. | 迁移条件、复现清单和研究计划。 / Transfer conditions, reproduction checklist, and research plan. |
| 局部解释 / Focused | 只关心一张图、一条公式或一段文字。 / You need one figure, equation, or passage explained. | 指定内容、必要背景和解释。 / Requested item, essential context, and explanation. |

## 阅读结果 / Reading outputs

完整精读会把关键设计选择、原始图表和必要公式放入同一条研究脉络中解释。
A close reading explains key design choices, original figures, and necessary equations within one research storyline.

解释单张图时，结果会说明图的用途、阅读顺序、各面板的观察结果及其支持的结论。
For a single figure, the response explains its purpose, reading order, panel observations, and supported conclusions.

定制技能默认交付可离线打开的 HTML 笔记，同时维护项目语料库。用户可以指定输出目录和其他格式。
The customized skill defaults to offline HTML notes and maintains a project-local corpus. Users can specify another output directory or format.

## 本地命令 / Local commands

复制完整技能文件夹后，先运行对应系统的程序并读取内置指南。
After copying the complete skill folder, run the executable for your system and read its bundled guide first.

```powershell
& "<skill-root>/norman-paper-reading.exe" guide
& "<skill-root>/norman-paper-reading.exe" list
& "<skill-root>/norman-paper-reading.exe" read references/reading-workflow.md
```

| 命令 / Command | 中文用途 | English use |
| --- | --- | --- |
| `extract` | 提取 PDF 文字和来源位置。 | Extracts PDF text and source locations. |
| `render` | 生成原始图表的页面图或局部图。 | Renders pages or crops of original figures. |
| `validate` | 检查已保存的报告和资源。 | Checks saved reports and assets. |
| `reader` | 将准备好的内容制作成 HTML 阅读版。 | Builds an HTML reading version from prepared content. |

通过 `extract --help`、`render --help`、`validate --help` 和 `reader --help` 查看各命令参数。
Use `extract --help`, `render --help`, `validate --help`, and `reader --help` to see their arguments.

该技能的本地程序适用于 Windows x64 和 macOS 的 Apple Silicon 或 Intel 机型。
The skill’s local executable supports Windows x64 and macOS on Apple Silicon or Intel.

### 作者与许可

作者：小红书 **N同学**；抖音 / B站 **耐心的N同学**。

## 来源

本地 PDF 辅助程序来自 [N-tongxue/norman-skill](https://github.com/N-tongxue/norman-skill/tree/main/norman-paper-reading)。本发布包的定制与第三方说明见 [THIRD_PARTY_NOTICES.md](../THIRD_PARTY_NOTICES.md)。

原作者为 N同学，小红书账号为 N同学，B站与抖音账号为耐心的N同学。技能的定制阅读规则综合以下参考，相关归属集中记录在文档中。

- 《计算机视觉科研入门》手册的关键词论证主线、术语表、12 项阅读卡和收益、机制、代价及失败分析维度。
- [S. Keshav 的 How to Read a Paper](https://systems.cs.columbia.edu/ds2-class/papers/keshav-paper.pdf)，用于分层阅读与假设、贡献和疑问的记录。
- [Jason Eisner 的 How to Read a Technical Paper](https://www.cs.jhu.edu/~jason/advice/how-to-read-a-paper.html)，用于自己的解释、理解难点和知识联系。
- [Michael Nielsen 的 Augmenting Long-term Memory](https://augmentingcognition.com/ltm.html)，用于带上下文、来源和主张归属的复习提问。
- [frontend-design 包内规则](vendor/frontend-design/SKILL.md)及其 [Apache-2.0 许可证](vendor/frontend-design/LICENSE.txt)，用于 HTML 设计与检查。
