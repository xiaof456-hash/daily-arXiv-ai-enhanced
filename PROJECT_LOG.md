# 📅 项目日志 - arXiv 论文速递助手

> 最后更新：2026-06-18

## 🎯 项目目标
每日自动爬取 arXiv 数学物理方向（math-ph, hep-th, math.AG 等）的最新论文，并通过 DeepSeek API 生成中文摘要，最终以网页形式展示。

## 🔗 重要链接
- **网页地址**：https://xiaof456-hash.github.io/daily-arXiv-ai-enhanced/
- **GitHub 仓库**：https://github.com/xiaof456-hash/daily-arXiv-ai-enhanced

---

## 📌 2026-06-18 进度记录

### ✅ 今日成就
1. **成功配置环境**：修复了 `run.yml` 路径错误和 YAML 缩进问题。
2. **解决权限问题**：添加 `TOKEN_GITHUB` 密钥，解决 Actions 推送 403 错误。
3. **修正爬虫代码**：修复 `arxiv.py` 缩进错误，添加调试日志，确保读取 `CATEGORIES` 环境变量。
4. **调整日期时区**：将爬取日期从 UTC 修改为北京时间（`TZ="Asia/Shanghai"`）。
5. **优化前端配置**：手动修改 `js/data-config.js` 中的 `repoOwner` 为 `xiaof456-hash`，解决数据 404 问题。
6. **验证数据内容**：确认数据文件包含 `math-ph`、`hep-th` 等分类，硬刷新后网页正常显示。

### 🔧 当前配置摘要
- **分类 (CATEGORIES)**：`math-ph, math.AG, math.QA, math.SG, math.AT, math.RT, math.DG, hep-th, hep-ph, gr-qc, quant-ph, cond-mat, nlin`
- **语言 (LANGUAGE)**：`Chinese`
- **定时任务**：每天 `UTC 1:30`（北京时间 9:30）自动运行
- **去重状态**：暂时跳过（`check_stats.py` 缺失，后续可优化）

### ⚠️ 注意事项
1. 如果网页数据未更新，请按 **`Ctrl+F5`**（Windows）或 **`Cmd+Shift+R`**（Mac）强制刷新浏览器缓存。
2. 若自动工作流失败，可登录仓库，在 `Actions` 选项卡手动点击 `Run workflow`。
3. 每天运行约消耗 0.2 元 DeepSeek API 费用（错峰时段）。

### 📝 待办事项（未来优化）
- [ ] 恢复去重功能，避免重复处理论文（节省 API 费用）。
- [ ] 调整 AI 摘要长度（`max_tokens` 参数）。
- [ ] 优化前端分类筛选器，确保正确显示所有自定义分类。

---

## 📅 历史记录

### 2026-06-17
- 初始 Fork 仓库，开始配置。
- 遇到大量 YAML 语法、路径、权限问题，逐一排查修复。
