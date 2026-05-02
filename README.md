# elko-brand-icons

**Curated brand SVG icon index for elko.ai reports.**

**4,305 companies** indexed — AI labs, tech giants, financial institutions, cloud providers, startups, and more. No SVG files stored here — just a lightweight JSON lookup that points to SVGs served from the [theSVG.org](https://thesvg.org) CDN.

---

## 🗂️ Files

| File | Size | Description |
|------|------|-------------|
| `brand-index.json` | ~2 MB | Full index — all 4,305 brands with all SVG variants |
| `brand-index-lite.json` | ~760 KB | Lightweight — slug → name + default SVG + brand color |

## 🔍 How to Use

### In HTML reports (inline SVG):
```html
<img src="https://cdn.jsdelivr.net/gh/glincker/thesvg@main/public/icons/openai/color.svg"
     width="24" height="24" alt="OpenAI">
```

### Via the JSON index:
```python
import json
with open("brand-index-lite.json") as f:
    brands = json.load(f)["brands"]

# Get any brand by slug
openai = brands.get("openai")
# → {"name": "OpenAI", "svg": "https://...", "color": "#000000"}
```

### In elko.ai reports (embed directly):
```html
<img src="{{brands[slug].svg}}" width="20" alt="{{brands[slug].name}}">
```

## 🎯 Coverage

| Category | Count |
|----------|-------|
| Software | 3,114 |
| Platform | 2,282 |
| Devtools | 597 |
| AI | 333 |
| Finance | 80 |
| Database | 108 |
| Security | 110 |
| Cloud | Included |
| All categories | 100+ |

## 📦 Source

All SVGs are hosted by [theSVG](https://thesvg.org) — a free, open-source library of 5,650+ brand SVG icons. CDN path pattern:

```
https://cdn.jsdelivr.net/gh/glincker/thesvg@main/public/icons/{slug}/{variant}.svg
```

Variants: `color`, `mono`, `dark`, `light`, `wordmark`

## 📄 License

This repo is a **referential index only**. All brand logos, names, and trademarks belong to their respective owners. The SVG files are served from theSVG.org's open-source collection. See [theSVG license](https://github.com/glincker/thesvg) for details.

---

*Built by [elko.ai](https://elko.ai) — AI Infrastructure. Local-First. AI Agnostic.*
