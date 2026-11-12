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

例如，输入“使用 `$paper-reading` 像严谨耐心的 AI 研究导师一样带我精读这篇论文，每轮围绕一个关键问题，读完后生成详细 HTML 笔记”。
For example, ask for mentor-led dialogue one reading unit at a time, followed by detailed HTML notes after the agreed scope is complete.

完整调用提示词见 [导师式精读提示词](assets/guided-reading-prompt.md)，互动流程见 [带读规范](references/guided-reading.md)。默认在对话中共同形成研究启示、下一步计划和论证表达语料，完成阅读后再汇总。笔记详细解释逻辑、方法、公式、证据和关键问答；图表使用经过检查的区域裁剪或原始单图。

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

定制技能默认先互动带读，在完成约定阅读与讨论后交付详细 HTML 笔记，并汇总项目语料库。用户明确要求直接总结、阶段笔记或其他格式时按其请求执行。
The skill defaults to guided dialogue, then detailed offline HTML notes and corpus consolidation after reading. Explicit direct-output or partial-note requests take priority.

## 本地命令 / Local commands

复制完整技能文件夹后，先运行对应系统程序的 version 命令，再读取本目录的 SKILL.md 和 references、assets 中的普通文件。
After copying the skill folder, check the runtime with version and read the local SKILL.md, references, and assets.

```powershell
& "<skill-root>/norman-paper-reading.exe" version
& "<skill-root>/norman-paper-reading.exe" extract --help
& "<skill-root>/norman-paper-reading.exe" render --help
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

## 输出检查

本包提供已清理的本地工作流、阅读模板和配置模板。程序内嵌指南属于旧实现，当前任务按 SKILL.md 和本地资源执行。最终 HTML 直接构建，交付前对实际笔记运行署名检查。

已开始的旧对话可能仍保留此前加载的规则。继续阅读时，应重新读取当前 `paper-reading/SKILL.md`，其中的对话迁移规则覆盖旧版署名要求，也适用于实验、基线和结果的简短追问。更新本地文件后，历史聊天消息仍保留原有内容。项目已有明确的输出规则时，继续遵循这些规则。

```sh
python scripts/check_output.py /path/to/reading-note.html /path/to/reading-note.md
python -m unittest discover -s tests -v
```

## 来源

本地 PDF 辅助程序来自 [N-tongxue/norman-skill](https://github.com/N-tongxue/norman-skill/tree/main/norman-paper-reading)。本发布包的定制与第三方说明见 [THIRD_PARTY_NOTICES.md](../THIRD_PARTY_NOTICES.md)。

原作者为 N同学，小红书账号为 N同学，B站与抖音账号为耐心的N同学。技能的定制阅读规则综合以下参考，相关归属集中记录在文档中。

- 《计算机视觉科研入门》手册的关键词论证主线、术语表、12 项阅读卡和收益、机制、代价及失败分析维度。
- [S. Keshav 的 How to Read a Paper](https://systems.cs.columbia.edu/ds2-class/papers/keshav-paper.pdf)，用于分层阅读与假设、贡献和疑问的记录。
- [Jason Eisner 的 How to Read a Technical Paper](https://www.cs.jhu.edu/~jason/advice/how-to-read-a-paper.html)，用于自己的解释、理解难点和知识联系。
- [Michael Nielsen 的 Augmenting Long-term Memory](https://augmentingcognition.com/ltm.html)，用于带上下文、来源和主张归属的复习提问。
- [frontend-design 包内规则](vendor/frontend-design/SKILL.md)及其 [Apache-2.0 许可证](vendor/frontend-design/LICENSE.txt)，用于 HTML 设计与检查。
- [安特卫普大学的 Socratic method 教学建议](https://www.uantwerpen.be/en/centres/centre-expertise-higher-education/didactic-information/teaching-tips/activating-students/socratic-method/)，用于提问后等待、依据回答给提示和调整问题层级。
