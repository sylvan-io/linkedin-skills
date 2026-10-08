# LinkedIn Marketing Skills（豆包版 · 零第三方依赖）

面向 LinkedIn 内容运营的 12 个豆包（Doubao）技能包：写帖子、写评论、回评论、去 AI 味、拆解爆款钩子、做一周内容计划、优化个人主页、团队员工倡导、跨平台改稿、素材采访等。

这是一组**零第三方依赖**的豆包（Doubao）技能包：不联网抓取、不自动发布、不调用任何外部 API。所有 LinkedIn 内容运营工作都在你与 agent 的对话中闭环完成。

- 📥 **内容输入由你手动提供**：把要处理的 LinkedIn 文字（帖子/评论/评论区/主页各段/互动者名单）粘贴进对话，或上传截图——技能不读取网络数据
- ✍️ **草稿由技能生成**：基于 2026 年算法与内容研究产出文案，等你回复「可以 / post / 修改建议」后定稿，不会自动改写或自动发布
- 📋 **发布由你手动完成**：技能交付「复制粘贴块」（最终文案 + 目标链接 + 手动操作步骤），由你粘贴到 LinkedIn 完成发布
- 🗂️ **技能即指令文件**：每个技能目录含独立的 `SKILL.md`，YAML frontmatter 声明 `name` + `description`，正文为给 agent 的纯指令；无 CLI、无 `.env`、无 API Key、无 Python 脚本，开箱即用

## 目录结构

```
linkedin-skills/
├── SKILL.md                          # 总入口：技能路由、核心流程、语气规则、URL/URN 速查
├── skills/
│   ├── linkedin-post-writer/         # 写帖子（20 种 2026 爆款钩子公式 + 创始人专属角度）
│   ├── linkedin-comment-drafter/     # 评论他人帖子 / 转发带评
│   ├── linkedin-reply-handler/       # 回复单条评论 / 批量清扫整个评论区
│   ├── linkedin-humanizer/           # 去 AI 味（重写 + 发布前审计 + 声音画像）
│   ├── linkedin-hook-extractor/      # 从爆款帖子反推钩子公式
│   ├── linkedin-content-planner/     # 7 天内容计划
│   ├── linkedin-thread-monitor/      # 追踪你的评论是否获得作者回复
│   ├── linkedin-engager-analytics/   # 互动者 ICP 分层（手动提供名单）
│   ├── linkedin-profile-optimizer/   # 主页审计与重写
│   ├── linkedin-employee-advocacy/   # 团队员工倡导计划
│   ├── linkedin-repurposer/          # 跨平台内容改稿（推文/视频/博客 → LinkedIn）
│   └── linkedin-interviewer/         # 采访你，沉淀「故事银行」素材
├── references/                       # 全包共享知识库（钩子公式、算法启发、语气规则等）
└── LICENSE · SECURITY.md · AGENTS.md · .gitignore
```

## 使用方式（统一流程）

1. **提供内容**：把要处理的 LinkedIn 内容粘贴进对话（帖子正文、评论、评论区、主页各段、互动者名单），或上传截图。
2. **起草**：技能基于 2026 年算法与内容研究生成草稿。
3. **确认**：你回复「可以 / post / 修改建议」，技能不会自动发布任何内容。
4. **手动发布**：技能交付复制粘贴块（最终文案 + 目标链接 + 操作步骤），由你粘贴到 LinkedIn 完成发布。

## 12 个技能一览

| 技能 | 作用 |
|---|---|
| **Post Writer** | 用 20 种经过验证的 2026 钩子公式（F1-F20，含创始人 A1-A10 角度）按互动目标写帖子 |
| **Comment Drafter** | 基于你粘贴的帖子写 1-3 条评论变体，附反应建议与模板归因 |
| **Reply Handler** | 回复单条评论，或整段评论区的批量清扫（过滤低质评论、正确处理 LinkedIn 两级线程扁平化） |
| **Humanizer** | 去除 AI 味：2026 词汇密度、reveal bridge、堆叠排比、表演式真诚；四遍处理 + 过度纠正保护；含发布前审计与声音画像 |
| **Hook Extractor** | 反推爆款帖使用的钩子公式，返回结构拆解 + 空白模板 |
| **Content Planner** | 7 天内容计划：支柱占比、钩子、CTA、发布时间、每日评论目标、周度就绪检查 |
| **Thread Monitor** | 判断你的评论是否被作者回复，按 6-24h 黄金回复窗口分级（hot/warm/cool/dormant） |
| **Engager Analytics** | 把互动者名单按 ICP 分层（同侪/进阶/潜在客户/其他），产出跟进动作清单 |
| **Profile Optimizer** | 九项主页组件审计（头像、横幅、标题、About、精选、经历、技能、URL、推荐）+ 重写 |
| **Employee Advocacy** | 14 天团队上线计划、发文节奏、品牌治理、ROI 度量 |
| **Repurposer** | 把推文/线程/视频/博客/通讯稿改写成原生 LinkedIn 帖子 |
| **Interviewer** | 采访你沉淀「故事银行」（角色、数字、转折点、伤疤、立场），所有写作技能共享 |



## 调用案例（每个技能怎么说）

在对话中直接说下面的触发语即可；需要内容的技能会向你索要粘贴文本或截图（安装后也可输入 `/` 或 `@` 技能名直接调用）。每个技能在你确认后都会交付复制粘贴块（或清单/报告），发布动作由你手动完成。

| 技能 | 触发语示例（直接对豆包说） | 你会得到 |
|---|---|---|
| **Post Writer** | 「帮我写一篇关于 CNC 加工精度的帖子，目标是获客」+ 粘贴素材 | 1-2 版草稿（900-1300 字符）+ 钩子公式依据；确认后复制粘贴块 |
| **Comment Drafter** | 「帮我写第一条评论」+ 粘贴目标帖子正文 | 1-3 条评论变体（200-350 字符）+ 推荐反应 |
| **Reply Handler** | 「给这条评论写个回复」/「把评论区值得回复的都扫一遍」+ 粘贴评论区 | 逐条回复草稿 + 低质评论过滤说明 |
| **Humanizer** | 「帮我去掉 AI 味」/「发布前审计一下」+ 粘贴草稿 | 重写文本 + 改动 diff + 每段 tell 密度（审计模式：Blockers / Warnings） |
| **Hook Extractor** | 「这帖子为什么火？钩子是什么公式」+ 粘贴爆款帖子 | 公式识别 + 有效原因 + 空白模板 |
| **Content Planner** | 「给我做一周内容计划，主题是 XX，面向 XX」 | 7 天计划表：支柱/格式/钩子/CTA/发布时间/评论目标 |
| **Thread Monitor** | 「我哪些评论被作者回复了」+ 粘贴你的评论记录 | hot / warm / cool / dormant 分级 + 跟进建议 |
| **Engager Analytics** | 「谁点赞评论了我的帖子，按客户画像分层」+ 粘贴互动者名单 | ICP 分层名单 + 跟进动作清单（回关/评论/DM 开场白） |
| **Profile Optimizer** | 「重写我的 headline 和 About」+ 粘贴主页各段 | 逐段重写 + 修改依据 |
| **Employee Advocacy** | 「给我们的市场团队做一个员工倡导计划」 | 14 天上线计划 + 发文节奏 + 品牌治理 + ROI 指标 |
| **Repurposer** | 「把这条推文改成 LinkedIn 帖子」+ 粘贴原文 | 原生 LinkedIn 版（重钩子、扩写、CTA、链接放首评） |
| **Interviewer** | 「采访我」/「这个帖子没素材，先采访我」 | 故事银行沉淀（角色/数字/转折点/伤疤/立场） |

**完整链路示例（Post Writer）**：

- 你：「帮我写一篇获客帖。素材：我们给德国客户做了 6061 铝合金腔体件，同心度做到 0.02mm。」
- 豆包：选择钩子公式起草，展示草稿与选择依据
- 你：「可以」
- 豆包：交付复制粘贴块（最终文案 + 目标链接 + 手动发布步骤）

## 安装到豆包

官方操作手册：[在豆包工作中使用技能](https://www.doubao.com/work/docs/zh-cn/articles/081010973544-skills)（豆包工作帮助中心）。技能文件格式遵循 [Agent Skills 规范](https://agentskills.io/specification)：每个技能目录含 `SKILL.md`，开头 YAML frontmatter 声明 `name` + `description`。

本仓库无任何代码依赖，开箱即用。安装步骤：

1. 打开豆包客户端，点击左侧 **插件·技能·伙伴**，切换到 **技能** 页面，点击右上角 **+ 添加**。
2. 选择 **上传技能**，直接上传本地技能文件或文件夹。
3. 选择要上传的目录：
   - **整包安装**：上传仓库根目录 `linkedin-skills/`，根 `SKILL.md` 作为路由入口，可调用全部 12 个子技能；
   - **单技能安装**：只上传 `skills/<技能名>/` 目录（如 `skills/linkedin-post-writer/`），单独使用该技能。
4. 豆包会校验 `SKILL.md` 的 YAML frontmatter；若字段不全或格式不规范，可让豆包工作帮忙检查或补充。
5. 安装完成后，在 **技能 → 我安装的** 中查看、替换或删除；在任务对话框中输入 `/` 或 `@` 搜索并调用目标技能。

> 注：技能无需安装也可在任务中直接使用；安装后平台会记住调用参数，便于下次复用。

## 许可

MIT。上游知识与数据出处：arXiv 2501.16450（360Brew 算法研究）、AuthoredUp 2026 触达数据、MagicPost 厂商数据等，均保留在各 reference 文件内。
