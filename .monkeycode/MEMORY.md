# 用户指令记忆

本文件记录了用户的指令、偏好和教导，用于在未来的交互中提供参考。

## 格式

### 用户指令条目
用户指令条目应遵循以下格式：

[用户指令摘要]
- Date: [YYYY-MM-DD]
- Context: [提及的场景或时间]
- Instructions:
  - [用户教导或指示的内容，逐行描述]

### 项目知识条目
Agent 在任务执行过程中发现的条目应遵循以下格式：

[项目知识摘要]
- Date: [YYYY-MM-DD]
- Context: Agent 在执行 [具体任务描述] 时发现
- Category: [代码结构|代码模式|代码生成|构建方法|测试方法|依赖关系|环境配置]
- Instructions:
  - [具体的知识点，逐行描述]

## 去重策略
- 添加新条目前，检查是否存在相似或相同的指令
- 若发现重复，跳过新条目或与已有条目合并
- 合并时，更新上下文或日期信息
- 这有助于避免冗余条目，保持记忆文件整洁

## 条目

[报告页面与配置页入口]
- Date: 2026-04-17
- Context: Agent 在执行“将项目改造成 AI 热点检测并部署预览”时发现
- Category: 代码结构
- Instructions:
  - 根目录 `index.html` 是对外展示的网页报告入口。
  - `trendradar/report/generator.py` 在生成报告时会同时回写 `output/index.html` 和根目录 `index.html`。
  - `docs/index.html` 是静态配置编辑器页面，适合单独预览配置体验。

[本地预览方式]
- Date: 2026-04-17
- Context: Agent 在执行“将项目改造成 AI 热点检测并部署预览”时发现
- Category: 构建方法
- Instructions:
  - 这个仓库可以直接用静态文件服务器预览，使用 `python3 -m http.server 8000` 即可访问根目录网页。
  - 当前环境没有 `uv` 命令，可优先使用 `python3` 相关命令进行验证和预览。
