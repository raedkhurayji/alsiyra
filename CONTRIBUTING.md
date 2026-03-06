# Contributing to مبادرة السيرة الرقمية

بسم الله الرحمن الرحيم

Thank you for contributing to this project. Every contribution is a sadaqah jariyah (صدقة جارية).

---

## Roles

| Role | Who | Responsibility |
|------|-----|----------------|
| **Contributor** | Anyone | Submits issues and pull requests |
| **Trusted Committer (TC)** | Core team | Reviews PRs, maintains quality, merges code |
| **Scholar** | Islamic scholars | Verifies all Islamic content before publishing |
| **Product Owner** | Project lead | Defines roadmap and priorities |

---

## Workflow

```
1. Open an Issue → describe what you want to do
2. TC approves the idea
3. Create a branch from develop
4. Make your changes
5. Open a Pull Request
6. 2 TC approvals required
7. TC merges into develop
8. TC merges develop → main on release
```

---

## Branch Strategy

```
main          ← stable, production only
develop       ← integration branch (all PRs go here)
  ├── feat/
  ├── fix/
  ├── content/
  ├── config/
  └── translation/
```

### Branch Naming

```
feat/short-description        new feature
fix/short-description         bug fix
content/chapter-01-import     content work
config/scholar-workflow       Drupal config
translation/en-chapter-01     translation work
docs/update-readme            documentation
```

---

## Commit Messages

We follow Conventional Commits:

```
type(scope): short description

Optional body explaining WHY

Closes #issue_number
```

### Types

| Type | Use for |
|------|---------|
| feat | New feature |
| fix | Bug fix |
| content | Content import or update |
| config | Drupal YAML config change |
| translation | Translation work |
| docs | Documentation only |
| refactor | Code cleanup |
| chore | Maintenance |

### Examples

```
feat(drupal): add chapter content type with moderation workflow
fix(api): correct basic auth header for JSON:API requests
content(ch01): import physical descriptions from pages 17-25
config(workflow): add scholar approval state to content moderation
translation(en): translate chapter 1 entities to English
```

---

## Content Rules

All Islamic content must follow these rules without exception:

1. Every hadith must include full source: e.g. أخرجه البخاري (635)
2. Every Quranic verse must include surah name and ayah number
3. Content must go through the Drupal editorial workflow — never directly to the database
4. Only scholar-approved content is published to the public API

### Content Lifecycle in Drupal

```
Draft → Under Review (Editor) → Scholar Review → Published
                                               → Rejected (with notes)
```

---

## Local Development Setup

Requirements: DDEV, Docker, Composer, Git

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

## Questions?

Open a GitHub Discussion or contact the Trusted Committer via GitHub Issues.

جزاكم الله خيراً
