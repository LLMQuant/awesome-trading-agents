---
name: "Remove entry · 移除条目"
about: "Request removal of a listed entry (link rot, archived, no longer LLM-driven, etc.) · 请求移除已收录条目"
title: "Remove: <repo-name>"
labels: ["removal"]
assignees: []
---

<!--
Use this template to request removal of a listed entry, OR to
request a move between sub-categories. For a sub-category boundary
change (new axis / merge / split), use the Restructure template
instead.
本模板用于请求移除已收录条目，或在子类之间重定位。子类边界本身
变更（新增 / 合并 / 拆分子类）请走 Restructure 模板。
-->

## 1. Entry being removed · 要移除的条目

- **Repo URL**: <!-- e.g. https://github.com/org/repo -->
- **Current sub-category in README**: <!-- e.g. `Agents → Multi-agent decision frameworks` -->

## 2. Removal reason · 移除原因

<!-- Tick all that apply. See CONTRIBUTING.md §5 / CONTRIBUTING.zh-CN.md §5 for the full criteria. -->

- [ ] Repo deleted or archived for >12 months without a clear successor.
- [ ] License changed in a way that contradicts CC0-1.0 reusability
      (move to `[Watch]` annotation rather than full removal may apply).
- [ ] No longer LLM-driven — refactored away from LLM reasoning as a
      primary decision component.
- [ ] Two-or-more failures on the §2 quality-bar checklist on
      re-evaluation.
- [ ] Other (explain in §4 below).

## 3. Evidence · 证据

<!--
Provide concrete evidence: the archive date, the commit that
removed LLM reasoning, the license-change commit, the dead-link
URL with a fetch error, etc. Maintainers re-verify before merging.
-->



## 4. Proposed action · 建议如何处理

<!-- Pick one. -->

- [ ] **Full removal** from the list.
- [ ] **Move to `[Watch]`** annotation in the same sub-category.
- [ ] **Move to a different sub-category** (specify):
      <!-- Target sub-category, en + zh dual label -->

## 5. Bilingual symmetric-edit reminder · 中英文同步提醒

<!--
Whoever lands the change in a PR must edit BOTH README.md and
README.zh-CN.md, OR open a tracked translation issue with a 7-day
SLA. See CONTRIBUTING.md §6 / CONTRIBUTING.zh-CN.md §6.
落地此变更的 PR 须同步改两份 README，或开 7 天 SLA 翻译跟踪 issue。
-->

## 6. Anything else · 其他信息

<!-- Optional: history, alternative entries that cover the gap, etc. -->
