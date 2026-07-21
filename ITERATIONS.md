# 迭代记录

## 2026-07-21

- 新增小红书链接的多方式提取规则：可见页面/搜索缓存、联网抓取 HTML、内嵌 JSON/state 检查、SRT 字幕下载、公开视频转录、`yt-dlp` 元数据探测。
- 明确小红书链接至少尝试 3 种真实提取方式后，才可以让用户粘贴字幕或文案。
- 将成功提取路径中的关键字段写入执行规则，包括 `noteDetailMap`、`mediaV2`、`subtitles`、`masterUrl`、`backupUrls`、`desc`、`title`、`nickname`、`tagList` 和互动数据。
- 同步更新 GitHub 发布所需文档：`README.md`、`README.zh-CN.md` 和 `ITERATIONS.md`。
