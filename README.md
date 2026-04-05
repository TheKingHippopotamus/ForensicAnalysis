<div align="center">

# Forensic Financial Research Reports

**Autonomous SEC filing analysis. No human in the loop.**

[![Live Site](https://img.shields.io/badge/live-thekinghippopotamus.github.io/ForensicAnalysis-22c55e?style=flat-square)](https://thekinghippopotamus.github.io/ForensicAnalysis/)
[![Pipeline](https://img.shields.io/badge/pipeline-Forensic__Analysis--ArelleMCP-e2b714?style=flat-square)](https://github.com/TheKingHippopotamus/Forensic_Analysis-ArelleMCP)

</div>

---

## Reports

| Ticker | Company | Filings Analyzed | Forensic Models | Transcript Quarters | Report |
|--------|---------|-----------------|-----------------|--------------------:|--------|
| **NKE** | NIKE, Inc. | 20+ | Beneish · Altman · Piotroski · Sloan · Benford | — | [View →](https://thekinghippopotamus.github.io/ForensicAnalysis/NKE/) |
| **RDDT** | Reddit, Inc. | — | — | — | *In progress* |

## How Reports Are Made

Each report is generated autonomously by the [SEC Forensic Research System](https://github.com/TheKingHippopotamus/Forensic_Analysis-ArelleMCP):

```
10-K / 10-Q / 8-K / DEF 14A / Form 4 / 13F / Earnings Transcripts
                              ↓
              13 parallel analysis agents
              6 forensic detection models
              10 transcript investigation layers
              31 research objectives covered
                              ↓
                    Unified HTML report
                              ↓
                  Published here via GitHub Pages
```

Every report covers: earnings quality, forensic scores, segment evolution, governance alignment, insider activity, management credibility, competitive positioning, supply chain risks, capital allocation, and forward predictions — all cross-validated across multiple data sources.

## Technical Details

- Reports are **self-contained HTML** files — no external dependencies
- Data source: **SEC EDGAR** (XBRL) + **q4cdn.com** (earnings transcripts)  
- Extraction: **[arelle-mcp](https://pypi.org/project/arelle-mcp/)** — 46-tool XBRL MCP server
- Analysis: **Claude Code** multi-agent orchestration
- Each report represents **200+ MCP tool calls** and **4,915 lines of analysis protocol**

---

<div align="center">
<sub>Built with <a href="https://github.com/TheKingHippopotamus/Forensic_Analysis-ArelleMCP">Forensic_Analysis-ArelleMCP</a> · <a href="https://pypi.org/project/arelle-mcp/">arelle-mcp</a> · <a href="https://github.com/TheKingHippopotamus">@TheKingHippopotamus</a></sub>
</div>
