# paper-reading

面向科研论文的阅读技能。以关键词串联研究问题、方法与证据，分析作者如何发现问题、为什么选择当前解法，生成可离线打开的 HTML 笔记，并持续积累论证与表达语料。

本仓库包含完整的独立发布副本，技能调用名为 `$paper-reading`。

## 功能

- 重建研究过程，区分作者明确披露的发现历史、论文中的论证和分析者推断。
- 按需求、已有做法、条件化缺口、原因假设、方法、验证、收益与边界组织解释。
- 阅读原始图表和必要公式，核对比较条件、证据强度、代价及失败情况。
- 结合研究入门手册与 Keshav、Eisner、Nielsen 的阅读方法，形成阅读卡、理解难点、知识联系和复习问答。
- 摘录逻辑组织与精准措辞，记录原文位置、中文解释、论证作用、提炼句式及使用条件。
- 使用 frontend-design 设计 HTML 阅读页面，检查导航、窄屏排版、公式、图表与复习交互。

## 阅读模式

| 模式 | 适用需求 | 内容范围 |
|---|---|---|
| Quick | 快速了解、判断阅读价值 | 简短关键词主线、关键结果、证据边界和复习重点 |
| Deep | 完整精读 | 研究过程、设计理由、图表公式、证据审查、笔记、语料与后续启发 |
| Extend | 迁移、复现规划 | 必要精读证据、适用条件、复现检查与可检验研究计划 |
| Focused | 指定图、公式或段落 | 所请求内容、必要背景及其证据边界 |

## 安装

在支持 skill-installer 的 Codex 中输入以下指令。

```text
$skill-installer https://github.com/kanfeng-eng/paper-reading-skill/tree/main/paper-reading
```

也可以下载仓库 ZIP，将完整的 `paper-reading` 文件夹复制到当前 AI 客户端的技能目录。包内 `vendor/frontend-design` 提供完整设计指导和许可证，客户端也可以调用已安装的同名技能。

## 使用

提供论文 PDF、可访问链接或论文标题，并说明阅读深度。

```text
使用 $paper-reading 精读这篇论文，抓住关键词并按逻辑串联。
重点说明作者如何发现问题、为什么这样设计方法，输出 HTML 笔记并收录值得学习的论证与表达。
```

```text
使用 $paper-reading 快速阅读这篇论文，重点判断研究问题、方法和证据，生成简洁 HTML 笔记。
```

## HTML 笔记与语料库

HTML 笔记默认保存在当前论文任务的项目目录中。

```text
项目目录/
├── 论文笔记/
│   └── 论文短名/
│       └── reading-note.html
└── 语料库/
    └── 论证与表达.md
```

完整 HTML 页面包括论文身份与范围、关键词逻辑主线、问题发现与解法选择、方法及图表公式分析、12 项阅读卡、理解难点、复习问答、语料选录、研究启发和来源。具体篇幅与所选模式一致。

页面内嵌样式、必要脚本和展示图片，核心内容可离线阅读。参考答案可逐项展开，重要结论和局限直接可见。语料累计文件用于跨论文维护，HTML 展示本次收录内容，稳定编号便于引用。用户明确指定其他格式、目录或仅在聊天中回答时，按实际请求执行。

## 包内文件与可移植性

```text
paper-reading/
├── SKILL.md
├── README.md
├── references/
│   ├── output-notes.md
│   ├── argument-expression-corpus.md
│   └── html-output.md
├── assets/corpus-template.md
├── vendor/frontend-design/
│   ├── SKILL.md
│   └── LICENSE.txt
├── norman-paper-reading.exe
├── norman-paper-reading-macos-arm64
└── norman-paper-reading-macos-x64
```

包内文件为普通副本，资源按技能目录或论文任务的项目目录定位。将完整技能复制到独立目录后即可读取规则并调用对应平台程序。打包目录 `other` 可在推送与安装完成后删除，已安装的原始技能与发布包分别保存。

Windows x64 和 macOS 的本地程序包含 PDF 处理运行组件。Linux 用户可由 AI 客户端提供可用的 PDF 提取和渲染工具。各平台均需要能读取文件、执行本地命令、分析论文和生成 HTML 的 AI 客户端，浏览器能力用于实际页面检查，联网检索依赖客户端提供相应工具。

macOS 从 ZIP 解压安装时，可在技能目录中为本机对应程序设置执行权限。

```sh
chmod +x norman-paper-reading-macos-arm64
# Intel Mac 使用 norman-paper-reading-macos-x64
```

辅助程序保留上游名称，内嵌指南也保留原始版本。本目录的 `SKILL.md` 和 `references/` 定义当前定制行为。程序入口示例见 [辅助程序说明](paper-reading/README.md)。

## 验证范围

发布前检查技能格式、相对引用、个人路径残留、链接文件及二进制一致性，并在独立副本中运行 Windows 辅助程序和内嵌资源读取。每篇论文的科学判断与 HTML 页面仍需在实际阅读任务中按技能要求核验。

## 第三方来源说明

本项目对 Norman Paper Reading 的阅读规则进行定制，并随包保留其 Windows 与 macOS 辅助程序及作者归属。frontend-design 副本随附 Apache-2.0 许可证。各组件的来源和许可记录见 [第三方说明](THIRD_PARTY_NOTICES.md)。

## 参考与来源

1. [N同学的 Norman Paper Reading](https://github.com/N-tongxue/norman-skill/tree/main/norman-paper-reading)，提供基础阅读工作流与本地 PDF 辅助程序。
2. 研究入门手册《计算机视觉科研入门》，提供关键词论证主线、术语表、12 项阅读卡以及收益、机制、代价和失败分析维度。相关结构已提炼到包内规则。
3. [S. Keshav 的 How to Read a Paper](https://systems.cs.columbia.edu/ds2-class/papers/keshav-paper.pdf)，提供分层阅读与假设、贡献、疑问记录方法。
4. [Jason Eisner 的 How to Read a Technical Paper](https://www.cs.jhu.edu/~jason/advice/how-to-read-a-paper.html)，提供面向未来自己的解释、理解难点和知识联系方法。
5. [Michael Nielsen 的 Augmenting Long-term Memory](https://augmentingcognition.com/ltm.html)，提供带上下文、来源和主张归属的复习提问方法。
6. [frontend-design 包内规则](paper-reading/vendor/frontend-design/SKILL.md)及其 [Apache-2.0 许可证](paper-reading/vendor/frontend-design/LICENSE.txt)，提供 HTML 页面设计、构建与复核指导。
