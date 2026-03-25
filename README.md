# RECCESSARY SEO / AEO Editorial Toolkit

SEO (Search Engine Optimization) and AEO (AI Engine Optimization) toolkit for the [RECCESSARY](https://www.reccessary.com) editorial team. Includes reference handbooks and Claude AI system prompts that editors can use to optimize articles before publication.

---

## Repository Structure

```
.
├── README.md
├── prompts/
│   ├── claude-artifact-prompt-en.md      # Claude Project prompt (English site)
│   └── claude-artifact-prompt-zh-tw.md   # Claude Project prompt (繁體中文站)
└── handbooks/
    ├── SEO-AEO-Handbook-EN-20260325.docx       # Full handbook (English)
    └── SEO-AEO-Handbook-ZH-TW-20260325.docx   # Full handbook (繁體中文)
```

---

## Quick Start: Setting Up the Claude Artifact

The Claude Artifact lets editors paste any article into a chat and receive a fully optimized version with diagnostics, explanations, and a pre-publish checklist.

### Step 1: Create a Claude Project

1. Go to [claude.ai](https://claude.ai)
2. In the left sidebar, click **Projects** > **Create Project**
3. Name it (e.g., "RECCESSARY SEO/AEO Optimizer - EN" or "RECCESSARY SEO/AEO 優化助手 - 中文")

### Step 2: Paste the System Prompt

- **For English site editors**: Copy the entire contents of [`prompts/claude-artifact-prompt-en.md`](prompts/claude-artifact-prompt-en.md) and paste it into the project's **Custom Instructions**
- **For 繁體中文站 editors**: Copy the entire contents of [`prompts/claude-artifact-prompt-zh-tw.md`](prompts/claude-artifact-prompt-zh-tw.md) and paste it into the project's **Custom Instructions**

### Step 3: Share with the Team

Click **Share** on the project and invite your editorial team members.

### Step 4: Start Using

Editors simply paste their article into the chat. They can optionally include:
- Target keyword
- Article URL
- Article type (paid/free)

Claude will automatically output:

| Output Section | Description |
|---|---|
| **Diagnostic Report** | Table listing all SEO/AEO issues with rule references |
| **Optimized Version** | Full article with changes in **bold**, data placeholders marked with `[🔢]` |
| **Change Explanations** | Item-by-item explanation of every change with rule numbers |
| **Pre-Publish Checklist** | ✅/❌/⚠️ judgment on every applicable rule |

---

## What the Prompt Covers

### Content Type Router

The prompt automatically detects the article type and adjusts rules accordingly:

| Content Type | Detection | Rule Adjustments |
|---|---|---|
| **Reccpedia** (encyclopedia) | URL contains `/reccpedia/` | All rules fully apply |
| **News** | URL contains `/news/`, short articles | Relaxed: H2 questions 30%+, FAQ/Key Takeaways optional for short articles |
| **Insight** (expert analysis) | URL contains `/insight/` | H2 questions relaxed to 40%+, E-E-A-T especially critical |
| **Interview** (Q&A) | URL contains `/interview/` | Direct quotes never rewritten, Q&A auto-satisfies H2 question rule |
| **Feature** (special reports) | URL contains `/feature/`, series | Series navigation links prioritized |
| **New Article** (from scratch) | Editor provides only a topic | Switches to generation mode: outline first, all data as placeholders |

### Rule Summary

| Rule | English Version | 繁體中文版 |
|---|---|---|
| **R1** Title Tag | Headline < 50 chars | 標題 < 20-25 字 |
| **R2** Meta Description | 120-155 chars | 75-90 字 |
| **R3** H2 Question Format | 50%+ (varies by type) | 50%+（依類型調整） |
| **R4** URL Slug | 3-5 English words | 3-5 英文字 |
| **R5** Internal Links | Min 3 (Hub + spoke + Reccpedia) | 至少 3 個 |
| **R6** Hub/Spoke Pages | `/en/` URLs | `/zh-tw/` URLs |
| **R7** Image SEO | Alt text with keyword | Alt text 含關鍵字 |
| **R8** Entity Naming | Consistent abbreviations | 用字一致性 |
| **A1** Instant Answer | Bold first sentence, 40-60 chars | 粗體首句，30-50 字 |
| **A2** Stats Density | Every 150-200 words | 每 200-300 字 |
| **A3** FAQ | 3-5 questions at bottom | 底部 3-5 題 |
| **A4** Comparison Table | When 2+ countries/options | 2+ 國家/選項時 |
| **A5** Key Takeaways | 3-5 items, each ≤ 20 words | 3-5 條，每條 ≤ 30 字 |
| **A6** Update Date | Visible "Last updated" | 可見「最後更新」 |
| **A7** E-E-A-T | Named author, .gov sources | 具名作者、官方來源 |
| **A8** Answer Formats | Definition/Comparison/List/Process | 定義/比較/列表/流程 |
| **A9** Originality | 1+ exclusive data point per article | 每篇 1+ 獨家數據 |
| **P1-P3** Paywall | Above-paywall structure & flow | Paywall 上方結構 |

### Data Safety

The prompt enforces a strict data policy:

- **Fixed facts** (institutional rules, historical events, regulatory thresholds): Can be used directly
- **Real-time data** (member counts, prices, market sizes, growth rates): Always uses `[🔢]` placeholders — never guesses from AI memory
- All placeholder data is collected into a "Data for Editor to Confirm" list with suggested sources

---

## Handbooks (.docx)

The handbooks are comprehensive reference documents for editorial teams. They contain:

1. **Pillar Page Inventory** — All existing pages that can be optimized, with real URLs
2. **Keyword Cluster Planning** — 4 clusters with hub/spoke architecture and top 20 target keywords
3. **SEO Writing Guide** — Title tags, meta descriptions, H2 formatting, internal linking, image SEO, Schema markup, localization notes
4. **AEO Writing Guide** — AI citation principles, structured answer formats, entity optimization, originality requirements, with BEFORE/AFTER case studies
5. **Pre-Publish Checklist** — Complete checklist covering SEO, AEO, images, internal links, and technical items
6. **Paywall Content Optimization** — Above-paywall structure, word count guidelines, editor execution flow
7. **AI-Assisted Writing Quality Guide** (繁體中文版) — Originality requirements, AI draft workflow, E-E-A-T for YMYL-adjacent topics

---

## Version History

| Date | Version | Changes |
|---|---|---|
| 2026-03-25 | 1.0 | Initial release: EN + ZH-TW handbooks and Claude prompts |

---

## License

Internal use only. RECCESSARY (Carbon Sight Inc.) All rights reserved.
