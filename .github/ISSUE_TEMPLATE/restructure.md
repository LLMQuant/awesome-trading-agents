---
name: "Restructure · 重构提议"
about: "Propose a sub-category boundary change (new axis / merge / split) · 提议子类边界变更"
title: "Restructure: <one-line description>"
labels: ["restructure"]
assignees: []
---

<!--
Use this template for proposals that change the v0.1 taxonomy
itself: a new sub-category (a new axis under an existing pillar),
merging two existing sub-categories, splitting an existing
sub-category, or renaming a sub-category. Sub-category churn
requires a maintainer-led re-enumeration pass — please file the
proposal here rather than relabel in a regular new-entry PR.
本模板用于提议子类边界变更：新增子类（新轴）、合并两个子类、
拆分子类、或重命名子类。子类边界变更需要维护团队带头做一轮
重新枚举，请走本模板而非直接在新增 PR 中改子类标签。
-->

## 1. Proposal type · 提议类型

<!-- Tick exactly one. -->

- [ ] **New sub-category** — propose a new axis under an existing pillar.
- [ ] **Merge** two existing sub-categories.
- [ ] **Split** one existing sub-category into two.
- [ ] **Rename** a sub-category (en label, zh label, or both).
- [ ] **Reorder** sub-categories (rare; only if count-based ordering changes).

## 2. Affected pillar · 涉及的分类

- [ ] Agents
- [ ] MCPs
- [ ] Skills
- [ ] Resources (Papers / Learn) · 参考资料

## 3. Current state · 当前状态

<!--
Quote the existing sub-category labels (en + zh dual label as in
the README) and describe the current boundary.
-->



## 4. Proposed state · 提议变更

<!--
Specify the proposed sub-category labels (en + zh) and the new
boundary definition. If the proposal is a new axis, give the one-
line definition that would go in the sub-section intro.
-->



## 5. Evidence · 证据

<!--
What entries would move? List repos by current sub-category and
target sub-category. Why is the current boundary insufficient?
Cite specific entries that don't fit cleanly.
-->



## 6. Impact · 影响范围

- **Number of entries affected**: <!-- e.g. 6 entries move from A to B -->
- **New `<a id>` anchors required**: yes / no
- **TOC count changes**: <!-- e.g. Agents 8 → 9, MCPs 7 → 7, Skills 8 → 8 -->
- **README headings affected**: <!-- list -->

## 7. Bilingual lockstep reminder · 中英文同步提醒

<!--
Any restructure that lands MUST update both README.md and
README.zh-CN.md atomically (en + zh sub-category labels, anchor
IDs, TOC counts, sub-category intro paragraphs). The bilingual-PR
rule is non-negotiable for restructures — restructures cannot use
the 7-day SLA exception path. See CONTRIBUTING.md §6 / CONTRIBUTING.zh-CN.md §6.
重构落地必须 README.md 与 README.zh-CN.md 原子化同步更新（en/zh
标签、锚 ID、TOC 计数、子类介绍段）。重构 PR 不适用 7 天 SLA
例外路径。
-->

## 8. Anything else · 其他信息

<!-- Optional: alternatives considered, history of the boundary, etc. -->
