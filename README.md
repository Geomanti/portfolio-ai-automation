# Portfolio — AI Automation

Personal portfolio page for **Anton Uralskii**, AI automation engineer.
Single self-contained HTML file — no build step, no dependencies, no external assets.

**Live:** https://geomanti.github.io/portfolio-ai-automation/

---

## Files

| File | Purpose |
|------|---------|
| `index.html` | The entire site. All CSS is inline in `<style>`, all markup in one file. |

Nothing else is required. Open `index.html` in a browser and it works.

---

## Structure of `index.html`

| Block | What lives there |
|-------|------------------|
| `:root` CSS variables | Colors, accent, type scale, max width, padding — **change the look here first** |
| `<header>` / hero | Name, one-line positioning statement, contact links |
| `#method` | "How I actually use AI" — six principle cards |
| `#work` | "Systems I designed, built and run" — project cards |
| `#stack` | "What I build with" — tool/language chips |
| `#background` | Where the production discipline came from |
| `#contact` | Closing call-to-action + mail/LinkedIn/GitHub links |
| `<script>` at bottom | Scroll reveal (`IntersectionObserver`) and nav highlighting |

### Theme

Dark by default (`--bg:#0a0a0b`, accent `--acc:#d8ff4a`).
To restyle, edit the variables in `:root` only — every rule references them.

### Adding a project card

Copy an existing card inside `#work`, then edit:

```html
<article class="card">
  <p class="mono">Category · year</p>
  <h3>Project name</h3>
  <p>What it does, in one or two sentences. Lead with the outcome, not the tech.</p>
  <ul>
    <li>Concrete, measurable detail</li>
    <li>Constraints you actually dealt with</li>
  </ul>
  <p class="mono"><a href="https://github.com/Geomanti/repo">Repository →</a></p>
</article>
```

Keep the `mono` class on small labels — it drives the uppercase/tracked-out style.

---

## Editing workflow

```bash
git clone https://github.com/Geomanti/portfolio-ai-automation.git
cd portfolio-ai-automation
# edit index.html
git commit -am "Update work section"
git push
```

GitHub Pages rebuilds automatically within ~1 minute of the push.

Preview locally before pushing:

```bash
python3 -m http.server 8000
# http://localhost:8000
```

---

## PDF version

Printable exports (light + dark) were generated from this page with a print
stylesheet and are kept separately in Documents. The HTML is the source of truth —
regenerate the PDFs after significant edits.

---

## Contact

- Email — uralskyanton@gmail.com
- LinkedIn — https://www.linkedin.com/in/anton-uralskii-994105284
- GitHub — https://github.com/Geomanti
