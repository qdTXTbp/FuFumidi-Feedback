# FuFumidi · 问题反馈

这里存放 **FuFumidi** 应用内的反馈：每一条反馈 = **一个 Markdown 文件**，放在 `issues/YYYY/MM/` 下。
同时会在 [Issues](https://github.com/qdTXTbp/FuFumidi-Feedback/issues) 里开一条对应议题，便于讨论与跟踪进度。

> 本仓库**公开可读**；写入只允许维护者（应用通过服务端代提交，客户端不持有任何写权限）。

## 反馈从哪来

| 来源 | 怎么用 |
|---|---|
| **应用内一键上传**（推荐） | FuFumidi → 设置 → 反馈：填分类/模块/严重度/标题/症状/复现步骤，勾选是否附带体检报告与诊断包，点「上传到仓库」。体检报告会自动脱敏（用户名、机器名、家目录）。 |
| **网页手动提交** | 直接开 [New Issue](https://github.com/qdTXTbp/FuFumidi-Feedback/issues/new/choose)，选对应模板填写。 |
| **离线兜底** | 网络不通时，应用会把 `feedback-<id>.zip`（含 `issue.md` + `health-report.md` + 可选 `diagnostic.zip`）存到本地，自己发到 Issues 或邮件附件即可。 |

## 每条反馈里有什么

```
issues/2026/10/2026-10-16-a1b2c3-<slug>.md
├── front-matter：id / 标题 / 分类 / 模块 / 严重度 / 版本 / 系统 / 显卡 / 安装方式 / install_id / 附件清单
├── 正文：症状 · 复现步骤 · 期望 vs 实际 · 频率
└── 折叠的体检报告（自动生成，已脱敏）
```

附件（诊断包 zip，含最近日志与设置）体积较大，**默认不上传**，由用户显式勾选；
上传后放在对象存储并给出限时链接，仓库里只留几十 KB 的文本。

## 隐私

- 体检报告在生成时就已经替换掉 **机器名、用户名、家目录**。
- **诊断包默认不上传**，且上传前会再过一遍脱敏（路径、令牌形状、曲库名）。
- 用户在上传前可以展开预览「将要上传的完整内容」。
- 反馈默认**匿名**：`install_id` 只是一枚随机 UUID，用于限流与去重，不与身份关联。
- 想要回复的话，在「联系方式」里留邮箱或 GitHub ID。

## 标签

| 前缀 | 取值 |
|---|---|
| `kind/` | bug · crash · perf · quality · idea · docs |
| `area/` | transcribe 转录 · score 变谱 · convert 转换 · voice 音色 · sing 调教 · play 播放 · library 曲库 · edit 编辑 · update 更新 · resources 资源中心 · other 其它 |
| `severity/` | blocker · major · minor |
| `source/` | app（应用内一键） · web（网页提交） |

## 目录

- `issues/YYYY/MM/` —— 应用上传的反馈文件（按年月分目录，避免单目录堆积）
- `.github/ISSUE_TEMPLATE/` —— 网页提交用的模板（字段与应用内一致）
- 反馈的处理结论会汇总回主仓库的 [`docs/known-issues.md`](https://github.com/qdTXTbp/FuFumidi/blob/release/5.0.0/docs/known-issues.md)
