# issues/

应用内的「反馈 → 上传到仓库」把每条反馈写在这里，**一人一个文件**，按年月分目录：

```
issues/2026/10/
├── 2026-10-16-a1b2c3-score-page2-fails.md
└── 2026-10-16-b7e9d1-playback-stutter.md
```

- 文件名：`YYYY-MM-DD-<6 位随机 id>-<ASCII slug>.md`（slug 取标题，≤40 字符，只含 `a-z0-9-`）。
- 文件里的 front-matter 与正文结构见上级 [README](../README.md)；同名冲突时追加 `-2`、`-3`。
- 这个目录**只增不改**：反馈内容一经提交就当作历史记录保留；后续讨论与结论放对应的 Issue。
