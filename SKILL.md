---
name: reference-video-script-rewriter
description: Turn a Chinese reference short-video link, transcript, or copywriting draft into a rewritten self-media spoken script. Use when the user asks to follow their 对标视频文稿流程, 获取原视频稿, 转述参考文案, 改写例子, 生成中文短视频逐字稿, or archive a finished script with title/cover/reference/original-idea sections.
---

# Reference Video Script Rewriter

## Core Promise

Convert one reference video or reference script into a publish-ready Chinese self-media draft by extracting the source, preserving the hook logic, rewriting examples, incorporating the user's own viewpoint, and archiving the result.

Default output target: 2-3 minute Chinese口播稿, unless the user requests another length.

## Workflow

1. Get the reference source.
   - If the user provides a link, try to open it and extract visible metadata: title, author, tags, stats, description, and public media URL.
   - If the page exposes a public video URL and ChatCut transcription tools are available, import only that selected video into a project and wait for transcription.
   - If automatic extraction fails, ask the user to paste subtitles or the reference copy.

2. Output the source script responsibly.
   - For long third-party transcripts, do not reproduce the entire source verbatim.
   - Provide a structured paraphrase in source order.
   - Include only a few short key original lines that are useful for preserving the hook and title logic.
   - Make clear when the source is paraphrased rather than exact transcript.

3. Ask for or use the user's own viewpoint.
   - Let the user state their framework, examples, personal observations, or changed angle.
   - Do not over-design a new thesis when the user wants early-stage pure copy转述.
   - Preserve the reference's strongest opening pain point or sentence pattern when useful.
   - Rewrite examples enough that they are not the same as the reference.

4. Generate the rewritten draft.
   - Start from the reference hook logic: common pain + concrete symptom + promise.
   - Keep the user's method names and examples when provided.
   - Use conversational Chinese with short speakable sentences.
   - Prefer practical frameworks, memorable labels, and concrete scenes.
   - Avoid sounding like a generic essay or a direct洗稿 version of the source.

5. Provide title and cover.
   - Main cover text: short, high-contrast, curiosity-driven.
   - Post title: use the reference's proven promise structure when appropriate.
   - Include a brief visual direction only if useful.

6. Archive when requested.
   - Create/use `内容/` in the current workspace.
   - Save as `YYYY-MM-DD_HHMM_帖子标题.md`.
   - Use this structure:
     - H1: post title
     - `## 标题与封面`
     - `## 逐字稿`
     - `## 参考视频链接和提取出来的文案`
     - `## 我的原始想法`

## Default Output Shape

When producing a full result, include:

- 标题与封面
- 逐字稿
- 参考视频链接和提取出来的文案
- 我的原始想法, if supplied

If the user has not chosen a title or cover, provide 5-8 title options and 1-2 cover directions. If the user has chosen them, use the chosen versions without reopening that decision.

## User Preference Notes

For this workflow, prioritize pure script transformation first. The initial goal is not full video production, editing, export, or cover rendering unless the user explicitly asks for those later.

The user's preferred process is:

1. 找到对标视频
2. 获取原视频稿
3. 输出或接收自己的独特想法
4. AI 修改文稿，尽可能保留原文开头吸引用户的原句，适当改写例子，不要跟参考文案完全一致，并给出封面设计和标题设计
5. 产出逐字稿
6. 后续人工或工具链继续录制、剪辑、字幕、封面和视频产出

## Example Archive Metadata

Use the current date and time for filenames. Example:

`内容/2026-07-20_0935_脑子里很多想法，一开口就乱？试试这 4 个方法.md`
