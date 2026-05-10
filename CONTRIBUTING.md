# Contributing

<p><strong>English</strong> · <a href="CONTRIBUTING.zh-CN.md">简体中文</a></p>

Thanks for helping improve **awesome-trading-agents**. This list is for people
who want to find real LLM-driven trading, investment, and financial-research
projects without sorting through older quant, time-series, or reinforcement
learning material.

> [!IMPORTANT]
> **AI-native contribution path:** after editing the list, add this file and
> the changed README file(s) to your Claude Code, Codex, Cursor, or other
> coding-agent session. Ask the agent to review the change against scope,
> quality bar, duplicate entries, bilingual sync, anchors, entry format, links,
> and `awesome-lint` output. Apply small fixes, then open the PR.

Useful review prompt:

```text
Review my awesome-trading-agents change. Check whether the entry is in scope,
meets the quality bar, duplicates an existing listing, keeps README.md and
README.zh-CN.md structurally synced, preserves anchors, follows the entry
format, and only treats awesome-lint output as advisory. Suggest minimal fixes.
```

## 1. Welcome and scope

This list covers the post-LLM, agentic stack for trading, investment, and
financial research:

- LLM-driven trading agents and multi-agent decision systems.
- Investment research, due-diligence, and market-monitoring copilots.
- MCP servers for market data, brokerage, execution, research, and backtesting.
- Claude Skills / Agent Skills for repeatable trading and finance workflows.
- Agent benchmarks, reference architectures, papers, and learning resources
  when they directly support the trading-agent stack.

Some useful projects belong elsewhere. We normally do not list classical quant
libraries, LSTM / Transformer / GNN price-prediction repos, deep-RL trading bots,
generic LLM tutorials, pure fintech infrastructure, or closed products without a
public technical artifact. The [Related awesome lists](README.md#related-awesome-lists)
section points readers to better homes for those areas.

## 2. Quality bar

The main list is selective because readers use it to save time. A new entry
should clear this checklist, or explain why a narrow exception is justified:

- [ ] **Open source**, or at least has a public technical artifact such as a
      paper, architecture doc, or reproducible demo.
- [ ] **Demonstrably LLM-driven**: LLM reasoning is a primary part of the
      research, decision, tool-use, or execution workflow.
- [ ] **Active or recently active**: normally updated in the last 12 months,
      unless it is a canonical paper, benchmark, or foundational reference.
- [ ] **Clear scope and minimal documentation** so a reader can understand what
      the project does and how it is used.
- [ ] **Distinct contribution** compared with nearby entries already in the
      list.
- [ ] **Public credibility signal**: repo entries normally need at least **100
      GitHub stars**, unless they are first-party artifacts from a recognized
      protocol, broker, exchange, data vendor, or canonical companion repos for
      listed papers / benchmarks.

The 100-star floor is a default, not a punishment for early projects. Smaller
repos are often better handled through an issue, a watch note, or a later
maintenance pass after more public adoption appears.

## 3. Submission format for new entries

The smoothest path is to open an issue with the
[Add entry](.github/ISSUE_TEMPLATE/add-entry.md) template. A direct PR is also
fine when the fit is obvious.

For each new entry, include:

1. **Repo URL**: the canonical primary URL, not a fork unless the fork is the
   project being listed.
2. **Pillar and sub-category**: pick an existing section from `README.md`; do
   not create a new sub-category in a routine entry PR.
3. **Entry bullet body** matching the local style:

   ```markdown
   - [org/repo](https://github.com/org/repo) - Concise description under 120 English chars. *(Optional pairing or lineage note.)*
   ```

4. **Submission-time metadata** in the PR description: GitHub stars and recent
   activity date (`YYYY-MM-DD`). Do not put per-entry star counts, activity
   dates, or temporary badges into the README row.
5. **Pairing annotation**, when useful: use `pairs with <name>` when the entry
   uses another listed artifact, or `used by <name>` when another listed
   artifact depends on it.
6. **Self-evaluation** against the quality-bar checklist in section 2.

## 4. Removal, moves, and restructuring

Use the [Remove entry](.github/ISSUE_TEMPLATE/remove-entry.md) template when an
entry appears stale, archived, deleted, no longer LLM-driven, or incorrectly
listed.

Use the [Restructure](.github/ISSUE_TEMPLATE/restructure.md) template when you
want to add, merge, rename, or split sub-categories. Category boundaries affect
navigation across both READMEs, so they are reviewed separately from routine
new-entry PRs.

Small moves between existing sub-categories can be proposed in an issue or PR,
but include the reason so maintainers can preserve the curation trail.

## 5. Removal criteria

An entry may be removed, moved, or marked for watch-list follow-up when one of
these becomes true:

- The repo is deleted or archived for more than 12 months without a clear
  successor.
- The project is no longer primarily LLM-driven.
- The public artifact disappears, becomes unusable, or turns into a closed
  product with no open code, paper, architecture note, or reproducible demo.
- The project no longer clears the main-list credibility floor during a
  maintainer review and has no documented first-party or canonical-companion
  exception.
- A re-evaluation finds multiple quality-bar failures that make the listing less
  useful to readers.

## 6. Bilingual README rule

The repo has two public README files:

- `README.md`: English, primary on the GitHub surface.
- `README.zh-CN.md`: Simplified Chinese.

They should stay in structural lockstep: same sections, same sub-categories,
same entry order, and matching `<a id>` anchors.

If a PR edits one README, it should edit the other in the same PR. If you cannot
write both languages, open a tracked translation issue with a **7-day SLA** and
link it in the PR description. Maintainers may hold the PR until the sibling
edit lands, or explicitly approve a single-side merge with follow-up tracking.

The two files do not need to be literal translations. Natural English and
natural Chinese are preferred, as long as the structure and meaning stay aligned.

## 7. Curation style and category boundaries

The README should read like a practical awesome list: project link, concise
description, and stable context that helps readers choose.

- Put official status in prose, such as "Alpaca's official MCP".
- List a cross-pillar project once in its primary section, then use a short
  cross-link only where the secondary angle is genuinely helpful.
- Mention fork lineage, shared authorship, or pairings only when it improves
  navigation.
- Keep maintainer first-read picks in the "If you only read three" block, not as
  badges beside every row.
- Do not add per-entry star counts, activity dates, or curation badges to the
  README row.

When a candidate could fit two sub-categories, choose the one whose current
heading and intro are the closer fit. If neither section fits, open a
Restructure issue instead of creating a new category inside a normal entry PR.

## 8. Awesome-lint and local checks

`awesome-lint` is useful, especially before opening a README PR:

```bash
npx --yes awesome-lint README.md
```

If you changed the Chinese README structure, you can also run:

```bash
npx --yes awesome-lint README.zh-CN.md
```

Treat the output as reviewer input, not an automatic merge gate. This repo uses
some local patterns that classic awesome lists may flag: stable `<a id>` anchors,
bilingual mirrors, compact pairing notes, cross-pillar back-links, and an image
header. Fix high-signal problems introduced by your PR, such as broken Markdown,
malformed links, accidental duplicate primary entries, misspellings, or rows
that no longer match the local entry format. Do not reformat the whole README
only to silence low-signal lint noise.

## 9. PR title & commit conventions

This repo follows [Conventional Commits](https://www.conventionalcommits.org/).
Because we **squash-merge** every PR, the **PR title becomes the subject of the
resulting commit on `master`** — so the PR title is the only thing that needs
to follow the format. Individual commits on a PR branch are unconstrained.

A GitHub Action (`.github/workflows/pr-title.yml`) validates every PR title
against the spec below. PRs whose title doesn't match cannot be merged.

### Format

```
<type>(<scope>): <subject>
```

### Types

| type       | when to use                                                    |
|------------|----------------------------------------------------------------|
| `docs`     | add / remove / edit list entries, README content               |
| `fix`      | dead link, typo, broken or misclassified entry                 |
| `style`    | formatting, CJK whitespace, pure layout                        |
| `chore`    | repo maintenance, dependency bumps                             |
| `ci`       | workflows, lint config, `.lycheeignore`                        |
| `refactor` | restructure or move existing entries / categories              |
| `feat`     | new section, new pillar, larger structural addition            |

### Scopes (optional)

`agents` · `mcp` · `skills` · `papers` · `en` · `zh-CN` · `ci` · `infra`

Small PRs may omit a scope (e.g. `fix: typo in intro`).

### Subject

- Imperative mood, lowercase first word (`add`, not `Added` or `Adds`).
- No trailing period.
- Fit within ~72 characters (GitHub UI truncates beyond this).
- English by default; Chinese acceptable for `zh-CN`-scoped changes.

### Examples

- `docs(agents): add HKUSTDial/DeepFund to benchmarks`
- `fix(mcp): remove archived foo-server entry`
- `style(zh-CN): add CJK spacing in DeepEar entry`
- `ci: ignore github topic pages in lychee`
- `chore: bump label set to v1.1`

## 10. Code of conduct

This project follows the
[Contributor Covenant v2.1](https://www.contributor-covenant.org/version/2/1/code_of_conduct/).
Please keep discussions respectful, assume good faith, and focus on the
technical and curation work. Maintainers may close threads that become personal,
repetitive, or unrelated to improving the list.

## 11. License notice

The list text, curation structure, README files, contribution guides, and PR
text contributed to this repository are released under [CC0-1.0](LICENSE). By
submitting a PR, you agree that your contribution to the list text is released
under CC0-1.0.

Each linked project keeps its own license. Listing a project here does not
change the license of the linked code or artifact.

Maintained by [LLMQuant](https://llmquant.com).
