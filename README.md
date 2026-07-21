# Reference Video Script Rewriter

Reference Video Script Rewriter turns a Chinese reference short-video link, transcript, or draft into a publish-ready self-media spoken script. It focuses on extracting the reference structure, preserving strong hook logic, rewriting examples, adding the user's viewpoint, and producing a concise Chinese talking-head draft with title and cover ideas.

## When to Use

Use this skill when you want to:

- Extract a reference video's metadata, transcript, or structure.
- Paraphrase a reference script responsibly instead of copying it.
- Preserve a strong opening hook while rewriting the body.
- Add your own angle, examples, framework, or observations.
- Generate a 2-3 minute Chinese spoken script.
- Produce title options, cover text, and a default archive file for complete results.

## What It Does

The workflow:

1. Collects the reference source, including title, author, tags, stats, description, video URL, and transcript when available.
2. For Xiaohongshu links, tries multiple extraction methods before asking for pasted subtitles:
   - visible page or web cache/search;
   - direct HTML fetch and embedded state inspection;
   - `noteDetailMap`, `mediaV2`, `subtitles`, `masterUrl`, `backupUrls`, `desc`, `title`, `nickname`, `tagList`, and interaction count extraction;
   - Chinese/source SRT subtitle download and duplicate comparison;
   - video download/transcription paths such as ChatCut when public media URLs are exposed;
   - command-line metadata tools such as `yt-dlp --dump-json` when installed.
3. Provides a structured paraphrase of long third-party transcripts, with only short key excerpts when useful.
4. Uses the user's own viewpoint when supplied.
5. Rewrites the script in conversational Chinese with short, speakable sentences.
6. Outputs title and cover ideas plus the final script.
7. Archives complete results to `内容/` by default unless the user explicitly says not to save.

## Installation

Place the skill folder at:

```text
~/.codex/skills/reference-video-script-rewriter
```

The repository root should contain:

```text
SKILL.md
README.md
README.zh-CN.md
ITERATIONS.md
agents/openai.yaml
```

## Example Prompt

```text
Use reference-video-script-rewriter on this Xiaohongshu reference video.
Extract the original transcript if possible, keep the opening hook, rewrite the examples so it is not identical, and output title/cover ideas plus a Chinese spoken script.
```

## Important Notes

- The default output target is a 2-3 minute Chinese talking-head script.
- For Xiaohongshu links, the agent should attempt at least three real extraction methods before asking the user to paste subtitles.
- When an extracted transcript or SRT exists, include a structured source-script treatment in source order, even when the user asks to directly rewrite.
- Complete results should be saved to `内容/` by default unless the user explicitly says not to archive.
- Do not reproduce long third-party transcripts verbatim; summarize in source order and quote only short hook or logic lines when needed.
- This skill is for script transformation first. It does not default to video production, editing, captioning, or export unless the user asks.

## Related Docs

- [中文说明](README.zh-CN.md)
- [迭代记录](ITERATIONS.md)
