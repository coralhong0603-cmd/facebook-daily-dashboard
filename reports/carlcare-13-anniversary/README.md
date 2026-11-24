# Carlcare 13周年 Facebook 活动看板（本地产物）

自包含静态看板，供发布到 GitHub Pages。不含任何 token / DM。

## 文件
- `index.html` — 中文看板（筛选/搜索/排序/图表/国家汇总表/明细/CSV导出），相对路径引用 `assets/`
- `posts.json` / `posts.csv` — 确定相关帖干净数据
- `pending.json` — 待确认候选与人审排除项（未计入汇总）
- `summary.json` — 汇总与口径
- `scan_audit.json` — 全量扫描审计（含未命中预览）
- `cache/raw_posts_since_2026-09-01.json` — 原始帖缓存（无 token）
- `build.py` / `update_round.py` — 只读 Graph API 扫描与生成脚本
- `assets/` — 帖子缩略图

## 口径摘要
- 扫描：27 主页（不含沙特/布基纳法索/马里），自 2026-09-01 起 `/posts` 分页
- 纳入：明确与 13 周年相关（Unlock 13、13th Anniversary、13 Years、13 Days of Care、13周年宣传视频、寻找隐藏数字13、周年互动谜题/答题/答案公布等）
- 排除：Men's Day、普通 Service Day、足球/赛事竞猜、日常 App 宣传、假期闭店、无关日常关怀图等
- 待定：仅凭文案/封面无法确认的疑似视频帖，不硬算进 confirmed
- Views：`post_media_view` lifetime；合计为各帖累计值相加（非去重触达）；缺失保留为 null，不填 0
- 互动：反应+评论+分享
- 每 post id 只计一次；不归因账号关注增长

## 更新 2026-11-24 10:57:36
- 确定相关 103 帖 / 17 主页；Views 83245（覆盖 103/103）；互动 5507（反应 2797 / 评论 2234 / 分享 476）
- 相对 2026-11-20 14:31:30（49帖 / 16页 / 33491 Views / 2118 互动）：帖 +54，主页 +1，Views +49754，互动 +3389
- 分类分布：Unlock13 89、关爱技巧 12、预热 1、周年视频 1
- 相对 11/20 新加入的参与国家：埃及
