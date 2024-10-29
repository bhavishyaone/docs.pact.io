# 📝 **Pact Docs Website**

[![Netlify Status](https://api.netlify.com/api/v1/badges/b5808ef1-8072-4687-84e8-2a0257f3ac8f/deploy-status)](https://app.netlify.com/sites/docs-pact-io/deploys)  
![Sync Pact docs](https://github.com/pact-foundation/docs.pact.io/workflows/Sync%20Pact%20docs/badge.svg)

---

## 📑 **Table of Contents**
- [💻 Local Development](#local-development)
- [➕ Adding Pages](#adding-pages)
- [➡️ Moving Pages](#moving-pages)
- [🔄 Automatic Syncing](#automatic-syncing-from-the-markdown-files-in-each-pact-implementation-repository)
- [💬 Slack History](#slack-history)
- [🌐 Hosting](#hosting)
- [🔍 Search](#search)
- [🤝 Contributing](#contributing)
- [📞 Contact](#contact)

---

## 💻 **Local Development**

The files are markdown, stored under the `docs` directory.  
**Requirements:** Docker and Docker Compose

**Command to Start:**  
```bash
docker-compose up
```

---

## ➕ **Adding Pages**

1. Place the new file in the correct path under `docs`.
2. Update the [sidebar JSON file](website/sidebars.json).

---

## ➡️ **Moving Pages**

1. Locate the file in the `docs` directory.
2. Move to the desired folder.
3. Update [sidebars.json](website/sidebars.json).
4. Update internal references, and create a redirect in [netlify.toml](netlify.toml).

---

## 🔄 **Automatic Syncing**

Markdown files in these directories sync automatically from their source repositories.  
* `docs/implementation_guides/go`
* `docs/implementation_guides/javascript`
* And more...

Whenever a markdown file is changed, the [sync-docs workflow](.github/workflows/sync-docs.yml) pulls it in and Netlify deploys the updates.

---

## 💬 **Slack History**

Slack message history is accessible via [docs.pact.io/slack/](https://docs.pact.io/slack/).

**Steps to Update Slack Export:**
1. Download the latest extract from Slack.
2. Use this [PHP script](https://gist.github.com/mefellows/1b825c86b2ff1063afbb2e5cb6b8cb3e) to convert it to HTML.
3. Sync HTML files to `website/static/slack`.

---

## 🌐 **Hosting**

The Pact Docs site is hosted by Netlify and redeploys on every push to `master`.

<a href="https://www.netlify.com">
  <img src="https://www.netlify.com/img/global/badges/netlify-dark.svg" alt="Deploys by Netlify" />
</a>

---

## 🔍 **Search**

Powered by Algolia! 🚀 Pact is an open-source project, allowing free use of Algolia's search capabilities.

1. Crawler defined [here](https://crawler.algolia.com/admin/crawlers/da3a74db-8003-4213-89d7-ae8c564cae42/overview)
2. Search configuration in `docusaurus.config.js`

---

## 🤝 **Contributing**

For guidance, see [CONTRIBUTING.md](CONTRIBUTING.md).

---

## 📞 **Contact**

* Join us on [Slack](https://slack.pact.io)
* Follow us on [Twitter](https://twitter.com/pact_up)

---
