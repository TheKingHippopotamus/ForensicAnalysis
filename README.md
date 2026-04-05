# ForensicAnalysis

Static HTML forensic research reports published via GitHub Pages.

**Live site**: [thekingbhippopotamus.github.io/ForensicAnalysis](https://thekingbhippopotamus.github.io/ForensicAnalysis/)

## Reports

| Ticker | Company | Status |
|--------|---------|--------|
| [NKE](./NKE/) | NIKE, Inc. | Phase 1-6 Complete |

## How Reports Are Generated

Reports are produced by the [Forensic_Analysis-ArelleMCP](https://github.com/TheKingHippopotamus/Forensic_Analysis-ArelleMCP) pipeline:

1. **Phase 0-1**: SEC XBRL extraction via arelle-mcp (46 tools)
2. **Phase 2-5**: Multi-agent forensic analysis (Beneish, Altman, Piotroski, Sloan, Benford's Law)
3. **Phase 7**: Earnings call transcript Q&A extraction
4. **Phase 8**: 10 parallel investigation layers (management decoder, credibility tracker, analyst intelligence, guidance forensics, competitive radar, supply chain, capital allocation DNA, customer growth, narrative drift, synthesis engine)
5. **Phase 6**: HTML report generation → pushed here

## Structure

```
ForensicAnalysis/
├── index.html          # Landing page with report index
├── .nojekyll           # Bypass Jekyll processing
├── NKE/
│   └── index.html      # NIKE forensic report
├── RDDT/               # (coming soon)
│   └── index.html
└── ...
```

Each report is a self-contained HTML file with embedded CSS, charts, and interactive navigation.
