# مبادرة السيرة الرقمية
### Digital Prophetic Biography Initiative

بسم الله الرحمن الرحيم

An open community endowment (وقف رقمي) to spread authentic knowledge about Prophet Muhammad ﷺ — verified by scholars, accessible to everyone, in every language.

---

## About

This platform transforms the book **"الموسوعة الميسرة في التعريف بنبي الرحمة ﷺ"** into a structured, searchable, multilingual Knowledge Graph — powered by AI extraction and verified by Islamic scholars.

**All content is:**
- Extracted by AI from verified Islamic sources
- Reviewed by editors
- Approved by a scholar before publishing
- Freely accessible via JSON:API

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| CMS | Drupal 11 |
| API | JSON:API |
| AI Extraction | Ollama + llava:13b |
| Local Dev | DDEV |
| Hosting | Ubuntu + Nginx |
| Version Control | GitHub |

---

## Getting Started (Local Development)

**Requirements:** DDEV, Docker, Composer, Git

```bash
git clone https://github.com/raedkhurayji/alsiyra.git
cd alsiyra
ddev start
ddev composer install
ddev drush config:import -y
ddev drush cr
ddev launch
```

---

## API

The platform exposes all verified content via JSON:API:

```
GET http://your-site/jsonapi/node/chapter
GET http://your-site/jsonapi/node/hadith
GET http://your-site/jsonapi/node/quranic_verse
```

---

## Contributing

We welcome contributions from everyone. Please read:

- [CONTRIBUTING.md](CONTRIBUTING.md) — how to contribute
- [GOVERNANCE.md](GOVERNANCE.md) — how decisions are made

This project follows the **InnerSource** methodology.

---

## License

GPL-2.0 — same license as Drupal.

---

*هذا المشروع صدقة جارية لنشر السيرة النبوية للعالم أجمع*
