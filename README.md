# 周周的报 · Weekly Insurance Report Skill

一个 Agent Skill：从 Google Drive 周文件夹里的 `URL Collection` 表格选文，逐篇写 180–250 字总结和公众号标题，按「标题说是什么，画面说怎么回事」的原则设计插图，用 punk-cover 生成，再排版写入 Google Doc《周周的报》。

栏目：保险创新 · 风险案列 · 融资 · 并购与合作 · 监管政策 · 相关新闻

## 安装

**Codex**
```bash
git clone https://github.com/HaoweiFan0912/zhouzhou-weekly-report.git
cp -r zhouzhou-weekly-report/zhouzhou-weekly-report ~/.agents/skills/
```

**Claude Code**
```bash
cp -r zhouzhou-weekly-report/zhouzhou-weekly-report ~/.claude/skills/
```

装好后，打开 `SKILL.md`，把 `<YOUR_DRIVE_FOLDER_ID>` 换成你自己 Google Drive 工作目录的文件夹 ID（文件夹链接里 `folders/` 后面那一串）。

然后说「写本周的周周的报」即可触发，Codex 里也可以用 `$zhouzhou-weekly-report`。

## 依赖

- Google Drive / Google Sheets 访问（连接器或 MCP）
- 网页读取（抓取工具或浏览器）
- punk-cover skill，需要装在同一个 skills 目录
- 图像生成工具（没有的话，插图位置会留出 prompt 占位）
- Python 和 `python-docx`

## 结构

```
zhouzhou-weekly-report/
├── SKILL.md                              # 主流程
├── agents/openai.yaml                    # Codex 的显示名称和默认提示
└── references/
    ├── illustration-examples.md          # 插图样例说明和画法总结
    └── examples/                         # 9 张参考插图
```
