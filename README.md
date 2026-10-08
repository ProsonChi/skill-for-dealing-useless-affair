# Skills for everyday tasks / 日常任务技能集

这个仓库用于收集可单独安装的 Codex 技能。每个技能位于独立文件夹，方便以后添加更多技能。

A collection of individually installable Codex skills. Each skill has its own folder so the repository can grow over time.

## Skills / 技能列表

| Skill | 用途 / Purpose |
| --- | --- |
| [Book review](book-review/SKILL.md) | 通读书籍，结合岗位与公司背景撰写读后感，润色并完成三轮自评。 / Read a full book, write a work-relevant reflection, polish it, and perform three self-review rounds. |

## Book review

为公司读书会撰写贴合个人工作背景的读后感。 / Write book-club reflections grounded in the reader's professional context.

## 中文介绍

Book review 是一个 Codex 技能，适合参加公司月度读书会的使用者。它先完整阅读你上传的书籍，再结合你的岗位职责、公司或行业背景，以及要求的字数范围，撰写适合分享的读后感。

使用前必须提供：

- 一本完整书籍文件，支持 PDF、EPUB、TXT、DOCX 或环境可以解析的其他格式。
- 你的岗位和主要职责。
- 所在公司的行业、业务或公司类型，无需真实公司名称。
- 读后感的字数上下限，例如 800 至 1200 字。

技能要求按章节通读全书，不能用简介、摘要或记忆代替。无法完整读取时，会停止撰写并请你上传页面齐全、可读取的 PDF。文章会结合工作情境分析书中观点，不虚构个人项目、业绩或经历。

初稿由 [humanizer](https://github.com/blader/humanizer) 润色，再由当前模型自行评审并调整三轮：核验内容与背景、改善自然表达、检查成稿逻辑与字数。不使用另一个评审模型，也不承诺通过 AI 作者身份检测。

### 安装与使用

将本仓库中的 `book-review` 文件夹放入 Codex 的技能目录（通常为 `~/.codex/skills`），并从上述上游仓库安装 `humanizer` 到同级目录。仓库不附带书籍，也不包含你的个人或公司资料。

上传书籍后，发送：

> 使用 $book-review。我的岗位是产品经理，主要负责需求分析和项目协调，公司从事企业软件行业。请写一篇 800 至 1200 字的读后感。

## English overview

Book review is a Codex skill for workplace book clubs. It reads the complete book you provide, then drafts a reflection tailored to your responsibilities, company or industry context, and requested length range.

Required inputs:

- A complete book file: PDF, EPUB, TXT, DOCX, or another format the environment can read.
- Your role and main responsibilities.
- Your company's industry, business, or type; the actual company name is optional.
- A minimum and maximum length. Specify the language and counting convention when requesting English or another language; the default is Chinese with a character-based count.

The skill must read the whole book in order. Summaries, excerpts, and prior knowledge are not substitutes. If the complete book cannot be read, it stops drafting and requests a complete, readable PDF. It connects the book's ideas to the user's work without inventing personal experiences or business results.

It applies [humanizer](https://github.com/blader/humanizer) and performs three self-review and revision rounds: source accuracy and professional relevance, natural expression, and final coherence and length. All reviews are performed by the current model. It makes no guarantee about AI-authorship detection.

### Installation and usage

Place the `book-review` folder in your Codex skills directory (typically `~/.codex/skills`). Install `humanizer` from its upstream repository as a sibling folder. No books, personal details, or company data are included in this repository.

Upload your book and send:

> Use $book-review. I am a product manager responsible for requirements analysis and project coordination at an enterprise software company. Write my reflection in English, between 600 and 800 words, using a word count.

## Repository layout / 仓库结构

```text
README.md
book-review/
  SKILL.md
  agents/
    openai.yaml
```

The workflow instructions are currently written in Chinese. / 技能流程说明目前使用中文。

## Dependency credit / 依赖说明

Natural-language editing uses [blader/humanizer](https://github.com/blader/humanizer), a separate MIT-licensed upstream project. Install that dependency separately; it is not redistributed here.
