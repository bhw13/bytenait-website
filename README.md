# BYTENAIT — Company Website

Landing page for [BYTENAIT](https://bytenait.com) · *Technology for Human Growth*

Built by Ben and Sam Wilt. Single-file static site — no build step, no dependencies.

---

## Files

| File | Description |
|---|---|
| `index.html` | Main landing page (all CSS + JS inline) |
| `opticram.html` | Opticram Vocab Engine interactive demo |

---

## Sections

- **Hero** — value proposition + CTA to demo
- **Who We Are** — founder story and stat cards
- **Our Mission** — mission statement and four pillars
- **What We're Building** — Opticram product suite (Vocab Engine, Math Engine, GMAT & SAT Expansion)
- **Footer / Contact** — email and LinkedIn

---

## Opticram Demo

`opticram.html` is a fully self-contained adaptive vocabulary demo. No backend required.

**Features:**
- 50 GRE words with spaced repetition scoring
- Three question types: Definition (MC), Context fill-in-the-blank, Write (sentence + definition)
- Adaptive engine promotes/demotes words based on performance
- Progress persisted in `localStorage`
- Waitlist popup triggers after question 3

---

## Waitlist Form (Formspree)

Email signups from the demo popup are handled by [Formspree](https://formspree.io).

**Current form endpoint:**
```
https://formspree.io/f/xaqpjaeb
```

**To update the form endpoint**, find this line in `opticram.html`:
```html
<form id="waitlist-form" action="https://formspree.io/f/xaqpjaeb" method="POST" ...>
```
Replace `xaqpjaeb` with your new Formspree form ID.

**To set up Formspree from scratch:**
1. Go to [formspree.io](https://formspree.io) and create a free account
2. Create a new form → copy the form ID from the endpoint URL
3. Replace the ID in `opticram.html` as shown above
4. Submissions will appear in your Formspree dashboard and can be forwarded to any email

**Formspree free tier limits:** 50 submissions/month. Upgrade at formspree.io if you exceed this.

---

## Deployment

Hosted on **GitHub Pages** with a custom domain via Squarespace DNS.

**Live site:** [bytenait.com](https://bytenait.com)

### Deploy changes

```bash
git add .
git commit -m "your message"
git push
```

GitHub Pages rebuilds automatically on every push to `master`. Changes are live within ~60 seconds.

### DNS records (Squarespace → GitHub Pages)

| Type | Host | Value |
|---|---|---|
| `A` | `@` | `185.199.108.153` |
| `A` | `@` | `185.199.109.153` |
| `A` | `@` | `185.199.110.153` |
| `A` | `@` | `185.199.111.153` |
| `CNAME` | `www` | `bhw13.github.io` |

### GitHub Pages settings

- **Source:** Deploy from branch → `master` → `/ (root)`
- **Custom domain:** `bytenait.com`
- **Enforce HTTPS:** enabled

---

## Design System

| Token | Value |
|---|---|
| Background | `#050505` |
| Accent green | `#00ff6a` |
| Amber | `#f59e0b` |
| Heading font | DM Serif Display |
| Body font | Instrument Sans |
| Mono font | JetBrains Mono |

Background animation is an L-system binary plant garden rendered on `<canvas id="binary-garden">`.

---

## Contact

**Email:** benjamin.h.wilt@bytenait.com
**LinkedIn:** [bhw13](https://www.linkedin.com/in/bhw13/)
**GitHub:** [bhw13](https://github.com/bhw13)
