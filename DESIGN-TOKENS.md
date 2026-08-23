# Design tokens — ForensicAnalysis

Extracted verbatim from the live site's `index.html` (`main` @ `52ab7db`, lines 12–36)
before the holding release replaced that file. These are the canonical palette and type
tokens for the site generator.

A machine-readable copy of the same block lives at `../design-tokens.css` (outside the repo).

## Homepage `:root` (verbatim)

```css
:root {
  --bg: #0B0E13;
  --bg2: #12161E;
  --bg3: #1A1F2B;
  --bg3h: #222838;
  --border: #262D3D;
  --border-light: #333C50;
  --t1: #F2EDE8;
  --t2: #9B9589;
  --t3: #6B665C;
  --green: #3D9B6E;
  --green-dim: rgba(61,155,110,0.12);
  --yellow: #C4A235;
  --yellow-dim: rgba(196,162,53,0.12);
  --red: #C4503A;
  --red-dim: rgba(196,80,58,0.12);
  --gold: #C9A227;
  --gold-bright: #E0B830;
  --gold-dim: rgba(201,162,39,0.10);
  --salmon: #D4836A;
  --blue: #6B8EBF;
  --blue-dim: rgba(107,142,191,0.10);
  --serif: 'Playfair Display', Georgia, 'Times New Roman', serif;
  --sans: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
}
```

## Report-page `:root` (verbatim, identical in all 13 report pages)

The report template (`FORENSIC REPORT TEMPLATE v3.0`) uses a second, differently-named
token set. Both were verified byte-identical across `AMD GOOGL INTC LLY META MSFT MU NVDA
RDDT TSLA UBER UUUU XOM`.

```css
:root {
  --bg-primary: #0a0e1a;
  --bg-secondary: #111827;
  --bg-card: #1a2234;
  --bg-card-hover: #1f2a40;
  --border: #2a3550;
  --text-primary: #e8edf5;
  --text-secondary: #8b99b0;
  --text-muted: #5a6880;
  --accent-green: #22c55e;
  --accent-green-dim: rgba(34,197,94,0.15);
  --accent-yellow: #eab308;
  --accent-yellow-dim: rgba(234,179,8,0.15);
  --accent-red: #ef4444;
  --accent-red-dim: rgba(239,68,68,0.15);
  --accent-blue: #3b82f6;
  --accent-blue-dim: rgba(59,130,246,0.12);
  --accent-purple: #a855f7;
  --accent-cyan: #06b6d4;
  --accent-orange: #f97316;
  --nav-width: 240px;
  --header-height: 90px;
  --font-serif: 'Playfair Display', Georgia, 'Times New Roman', serif;
  --accent-gold: #C9A227;
  --accent-gold-dim: rgba(201,162,39,0.10);
}
```

## Rules for the generator

- **No webfonts.** `Playfair Display` was previously loaded from a third-party font host.
  The holding release removed every such `<link>`. Keep `--serif` / `--font-serif` as they
  are: the Georgia / Times fallback renders with zero external requests. Do not re-add a
  font-host `<link>` or `@import`.
- **Two token namespaces.** Homepage uses `--bg/--t1/--gold`; report pages use
  `--bg-primary/--text-primary/--accent-gold`. `--gold` (`#C9A227`) is the one value shared
  by both and is the site's signature accent.
- `--border` exists in both namespaces with **different** values (`#262D3D` homepage,
  `#2a3550` reports). Do not merge the two sets without renaming.
