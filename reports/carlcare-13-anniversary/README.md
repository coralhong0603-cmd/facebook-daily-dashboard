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

## 更新 2026-11-25 16:20:55
- 确定相关 128 帖 / 17 主页；Views 98484（覆盖 128/128）；互动 6361（反应 3264 / 评论 2559 / 分享 538）
- 相对 2026-11-24 10:57:36（103帖 / 17页 / 83245 Views / 5507 互动）：帖 +25，主页 +0，Views +15239，互动 +854
- 分类分布：Unlock13 111、关爱技巧 12、周年视频 2、周年优惠 2、预热 1
- 相对上一快照新加入的参与国家：无
