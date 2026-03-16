# QBS Documentation Site

Built with [Jekyll](https://jekyllrb.com/) and the [Just the Docs](https://github.com/just-the-docs/just-the-docs) theme, deployed via GitHub Pages.

---

## 🚀 Publishing to GitHub Pages

**1. Create a GitHub repo** — go to [github.com/new](https://github.com/new), name it `qbs-docs`, set it **Public**.

**2. Push this project:**
```bash
git init
git add .
git commit -m "Initial QBS docs"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/qbs-docs.git
git push -u origin main
```

**3. Enable GitHub Pages** — repo Settings → Pages → Source: **GitHub Actions** → Save.

**4. Update `_config.yml`:**
```yaml
baseurl: "/qbs-docs"
url: "https://YOUR-USERNAME.github.io"
```

Your site will be live at `https://YOUR-USERNAME.github.io/qbs-docs` within ~2 minutes.

---

## 📁 Structure

```
qbs-docs/
├── _config.yml
├── Gemfile
├── index.md                          # Homepage
├── .github/workflows/deploy.yml      # Auto-deploy
├── assets/images/accounting/         # Screenshots
└── docs/
    ├── accounting/                   # GL, COA, Voucher Type, Financial Year
    ├── bank-cash/                    # Bank, Branch, Account, Transactions
    ├── setup/                        # Division, District, Area, Business Type
    └── customers/                    # Customer, Supplier
```

## ✏️ Adding New Pages

Create a `.md` file in the relevant `docs/` folder with front matter:
```yaml
---
layout: default
title: My New Page
parent: Accounting
nav_order: 6
---
```

## 🖼️ Adding Screenshots

Place images in `assets/images/accounting/` and reference:
```markdown
![Alt text]({{ site.baseurl }}/assets/images/accounting/your-image.png)
```
