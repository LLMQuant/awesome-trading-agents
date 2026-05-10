# 贡献指南

<p><a href="CONTRIBUTING.md">English</a> · <strong>简体中文</strong></p>

感谢你愿意改进 **awesome-trading-agents**。这份清单服务的是想快速找到
LLM 驱动交易、投资和金融研究项目的读者，所以我们会尽量把真正相关、
可复用、还值得读的项目放进来，也会把传统量化、时间序列和强化学习交易
方向留给更合适的清单。

> [!IMPORTANT]
> **推荐的 AI-native 提交流程：**改完清单后，把本贡献指南和你改动过的
> README 文件一起放进 Claude Code、Codex、Cursor 或其他 coding-agent
> session，让它帮你检查：是否符合收录范围、质量门槛、是否和已有条目重复、
> 中英文 README 是否同步、锚点和条目格式是否正确、链接是否可用，以及
> `awesome-lint` 输出里哪些值得处理。做完小修后再开 PR。

可以直接把下面这段发给你的 coding agent：

```text
请帮我 review 这次 awesome-trading-agents 的改动。重点检查：条目是否在
收录范围内，是否满足质量门槛，是否和现有条目重复，README.md 与
README.zh-CN.md 的结构是否同步，锚点是否保留，条目格式是否符合本仓库
习惯，以及 awesome-lint 输出里哪些是需要修复的高信号问题。只建议必要的
小改动。
```

## 1. 欢迎与范围

这份清单关注 LLM 之后的交易智能体栈，主要包括：

- LLM 驱动的交易 Agent 和 Multi-agent 决策系统。
- 投研、尽调、盯盘和市场研究类 copilots。
- 面向行情、券商、交易执行、研究工具和回测的 MCP servers。
- 用于交易和金融工作流的 Claude Skills / Agent Skills。
- 直接服务 trading-agent stack 的评测、参考架构、论文和学习资源。

有些项目很好，但不一定属于这里。经典量化库、LSTM / Transformer / GNN
价格预测仓库、深度强化学习交易 bot、通用 LLM 教程、纯金融基础设施，
以及没有公开技术 artifact 的闭源产品，通常不放进本清单。README 的
[Related awesome lists](README.zh-CN.md#related-awesome-lists) 里会给这些
方向更合适的入口。

## 2. 质量门槛

主清单会保持一定筛选强度，因为读者来这里是为了节省时间。新增条目最好能
满足下面这些条件；如果有特殊原因，也请在 PR 里解释清楚：

- [ ] **开源**，或至少有公开技术 artifact，例如论文、架构文档或可复现实验。
- [ ] **明确由 LLM 驱动**：LLM 推理是研究、决策、工具调用或执行流程里的
      主要部分，而不只是事后解释或普通特征处理。
- [ ] **近期仍活跃**：仓库通常应在过去 12 个月内有更新；经典论文、benchmark
      或基础参考项目可以例外。
- [ ] **范围清楚、有基本文档**：读者能看懂它解决什么问题，以及大概怎么用。
- [ ] **和已有条目有明显区别**，不是同一类项目的重复收录。
- [ ] **有公开可信度信号**：仓库条目通常需要至少 **100 GitHub stars**。
      认可协议、券商、交易所、数据厂商的一方 artifact，或已收录论文 /
      benchmark 的 canonical companion repo，可以由维护者例外处理。

100-star 不是对早期项目的否定，只是主清单的默认信噪比要求。更早期的项目
可以先通过 issue、watch 说明，或后续维护轮次再进入主清单。

## 3. 新增条目的提交方式

最顺的方式是先开一个 [Add entry](.github/ISSUE_TEMPLATE/add-entry.md)
issue。若条目明显符合范围，也可以直接开 PR。

新增条目请尽量补齐这些信息：

1. **Repo URL**：项目的 canonical 主链接。除非 fork 本身就是要收录的项目，
   否则不要填普通 fork。
2. **Pillar 和 sub-category**：从现有 `README.zh-CN.md` 章节里选一个最贴近的
   小类。常规新增 PR 不要顺手创建新小类。
3. **条目正文**：遵循 README 里的本地格式：

   ```markdown
   - [org/repo](https://github.com/org/repo) - 80 字以内的中文简介。*(可选：pairing 或 fork 关系说明。)*
   ```

4. **提交时元信息**：在 PR 描述里写明 GitHub stars 和最近活动日期
   (`YYYY-MM-DD`)。不要把每个项目的 stars、日期或临时徽标写进 README 行内。
5. **搭配关系**：如果有帮助，可以说明它 `pairs with <name>`，或说明它
   `used by <name>`。
6. **质量门槛自评**：按第 2 节 checklist 简短说明。

## 4. 移除、移动和重构

如果某个条目已经失效、归档、删除、不再 LLM-driven，或明显放错位置，请使用
[Remove entry](.github/ISSUE_TEMPLATE/remove-entry.md) 模板。

如果你想新增、合并、重命名或拆分 sub-category，请使用
[Restructure](.github/ISSUE_TEMPLATE/restructure.md) 模板。分类边界会影响两份
README 的导航，不适合混在普通新增条目的 PR 里顺手改。

如果只是把一个条目在现有小类之间移动，可以开 issue 或 PR，但请写明原因，方便
维护者保留判断过程。

## 5. 移除标准

出现下面任一情况时，条目可能会被移除、移动，或转入后续 watch / 复核：

- 仓库删除，或归档超过 12 个月且没有明确 successor。
- 项目已经不再主要由 LLM 驱动。
- 公开 artifact 消失、不可用，或项目变成没有公开代码、论文、架构说明、
  可复现 demo 的闭源产品。
- 维护者复核时发现项目已低于主清单可信度门槛，且没有一方 artifact 或
  canonical companion repo 之类的明确例外理由。
- 重新评估时发现多个质量门槛失败，继续保留会降低读者体验。

## 6. 双语 README 规则

本仓库有两份公开 README：

- `README.md`：英文，GitHub 默认展示入口。
- `README.zh-CN.md`：简体中文。

两份 README 应保持结构同步：章节一致、小类一致、条目顺序一致、`<a id>` 锚点一致。

如果一个 PR 改了其中一份 README，原则上应在同一个 PR 里同步另一份。如果你暂时
只能写一种语言，请开一个带 **7 天 SLA** 的翻译跟踪 issue，并在 PR 描述中链接它。
维护者可以等另一份同步后再合并，也可以明确批准先合并一侧，再用跟踪 issue 补齐。

两份 README 不需要逐句硬翻译。英文应该像自然英文，中文也应该像自然中文；只要结构
和含义对齐即可。

## 7. 策展风格和分类边界

README 应该像一份好用的 awesome list：项目链接、简洁描述、少量稳定且有助判断的
上下文。

- 官方项目就在描述里自然写出来，例如 "Alpaca 官方 MCP"。
- 跨支柱项目只在主归属章节完整列一次；次要视角确实有帮助时，用短回链即可。
- fork 关系、同作者关系、搭配关系，只在能帮助读者导航时写。
- 维护者推荐的首读项目放在 "如果你只读三个" 区块，不要给每条都加徽标。
- 不要在 README 条目行内加入每个项目的 stars、活动日期或临时策展标签。

如果一个候选项目能放进两个小类，优先选当前标题和导语更贴近的那个。若现有小类都
不合适，请开 Restructure issue，而不是在普通新增 PR 里直接新建分类。

## 8. Awesome-lint 和本地检查

改 README 时，`awesome-lint` 很适合做一次辅助检查：

```bash
npx --yes awesome-lint README.md
```

如果你改了中文版 README 的结构，也可以跑：

```bash
npx --yes awesome-lint README.zh-CN.md
```

请把输出当作 reviewer input，而不是自动阻塞合并的硬门槛。本仓库有一些本地约定：
稳定 `<a id>` 锚点、双语镜像、紧凑 pairing 说明、跨支柱回链、图片 header。
这些可能会让传统 awesome-list linter 报出低信号提示。

如果 PR 新引入了高信号问题，应当修复：Markdown 损坏、链接格式错误、意外重复主条目、
拼写问题、条目不符合本仓库格式等。不要为了消除低信号 lint 噪音而大规模重排 README。

## 9. PR 标题与 commit 约定

本仓库遵循 [Conventional Commits](https://www.conventionalcommits.org/)。
由于我们对所有 PR 使用 **squash-merge**，**PR 标题就是 master 上 squash
commit 的 subject**——所以只需要约束 PR 标题；PR 分支内部的细节 commit
不受约束。

`.github/workflows/pr-title.yml` 会自动校验每个 PR 标题。不符合规范的 PR
无法合并。

### 格式

```
<type>(<scope>): <subject>
```

### Types

| type       | 适用场景                                              |
|------------|-------------------------------------------------------|
| `docs`     | 增删改清单条目、README 内容                           |
| `fix`      | 死链、错别字、错误条目                                |
| `style`    | 排版、中英文空格、纯格式                              |
| `chore`    | 仓库维护、依赖升级                                    |
| `ci`       | workflows、lint 配置、`.lycheeignore`                 |
| `refactor` | 调整或移动现有条目 / 分类                             |
| `feat`     | 新章节、新支柱、较大结构性添加                        |

### Scopes（可选）

`agents` · `mcp` · `skills` · `papers` · `en` · `zh-CN` · `ci` · `infra`

小型 PR 可不带 scope（例：`fix: typo in intro`）。

### Subject

- 祈使句首词小写（`add`，不是 `Added` / `Adds`）。
- 末尾不加句号。
- 控制在 ~72 字符以内（GitHub UI 截断阈值）。
- 默认英文；scope 为 `zh-CN` 的纯中文修改可使用中文。

### 示例

- `docs(agents): add HKUSTDial/DeepFund to benchmarks`
- `fix(mcp): remove archived foo-server entry`
- `style(zh-CN): add CJK spacing in DeepEar entry`
- `ci: ignore github topic pages in lychee`
- `chore: bump label set to v1.1`

## 10. 行为准则

本项目遵循
[Contributor Covenant v2.1](https://www.contributor-covenant.org/version/2/1/code_of_conduct/)。
讨论时请保持尊重、善意推断，尽量聚焦技术和策展问题。若讨论变成人身化、重复拉扯，
或偏离如何改进清单，维护者可能会关闭相关 thread。

## 11. 许可证说明

本清单文本、策展结构、README、贡献指南，以及贡献者提交到本仓库的 PR 文本，均以
[CC0-1.0](LICENSE) 发布。提交 PR 即表示你同意你对清单文本的贡献以 CC0-1.0 发布。

每个被链接的项目保留自己的许可证。被本清单收录，不会改变原项目代码或 artifact 的
许可证。

维护方：[LLMQuant](https://llmquant.com)。
