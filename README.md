# Linux Access Hugo Theme

**Linux Access** is an accessibility-first Hugo theme built to power a multi-author website focused on Linux and inclusive tech. This theme prioritizes screen reader support, semantic markup, and minimal but readable design.

---

## 🌟 Features

- Accessible-first layout with semantic HTML and Tailwind CSS
- Articles with author bios, tags, and summaries
- Custom shortcodes: `note`, `warn`, `kbd`, `button`, `callout`, `youtube`
- Authors section with profile pages and article listings
- FAQ page using accessible `<details>/<summary>`
- Client-side search in Articles section
- Hugo Module ready (import via GitHub)
- Clean typography with Tailwind's `prose` classes

---

## 🚀 Getting Started

### 1. Install Theme as a Hugo Module
Add this to your site’s `config.toml`:
```toml
[module]
[[module.imports]]
path = "github.com/yourusername/linux-access"
```

> Replace `yourusername` with the actual GitHub username.

During local dev:
```toml
[[module.replacements]]
path = "github.com/yourusername/linux-access"
replacement = "../linux-access"
```

---

## 🧱 Content Structure

### Articles
Markdown files in `content/articles/`:

```yaml
---
title: "Example Title"
date: 2025-03-31
author: "alex"
tags: ["tools", "accessibility"]
summary: "A quick look at accessible tools."
---
```

### Authors
Data files in `data/authors/`:

```yaml
name: "Alex Rivera"
bio: "Accessibility advocate and open source fan."
```

### FAQ
Create `content/faq.md`:

```yaml
---
title: "FAQ"
layout: "faq"
faq:
  - question: "How do I install Orca?"
    answer: "Use your package manager: `sudo apt install orca`."
---
```

---

## 🧩 Custom Shortcodes

- `{{< note >}}Info here{{< /note >}}`
- `{{< warn >}}Be careful{{< /warn >}}`
- `{{< kbd keys="Ctrl+Alt+T" >}}`
- `{{< button link="/faq" >}}Read FAQ{{< /button >}}`
- `{{< callout icon="🛠" title="Tip" >}}Try espeak-ng{{< /callout >}}`
- `{{< youtube id="abc123" title="Intro" >}}`

---

## 🛠 Dev Notes

- CSS in `assets/css/main.css`
- Tailwind config in `tailwind.config.js`
- Shortcodes in `layouts/shortcodes/`
- Templates in `layouts/`

---

## 🤝 Contributing

- Follow accessibility-first principles
- Keep layout markup semantic (use `<main>`, `<article>`, `<nav>`)
- Always test keyboard navigation
- Use screen reader testing where possible

---

## 📄 License

MIT — feel free to use, fork, and contribute!