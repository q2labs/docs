# q2-lab-doc

```markdown
# Documentation Writing Guidelines

Follow these guidelines when contributing or writing `.mdx` documentation pages.

---

### 1. Frontmatter
Every documentation file must start with YAML frontmatter:

```yaml
---
title: "Page Title | Q2Labs Documentation"
description: "A concise 1-2 sentence overview of what this guide covers."
slug: "/documentation/category/page-name"
category: "Category Name"
order: 1
canonical_url: "https://q2labs.ai/documentation/category/page-name"
---
```

---

### 2. Heading Structure & Table of Contents
* **Single `# H1`:** Use `# Heading` only once at the top for the page title.
* **Use `## H2` for Sections:** All `##` headings are automatically extracted into the **"On this page"** sidebar navigation.
* **Use `### H3` for Subsections:** For nested points under an `##` section.

---

### 3. Callout Boxes
Use the `<Callout>` component to highlight important context. **Do not add emojis** into the callout text—icons and brand theme colors are rendered automatically.

#### Available Callout Types:

* **Info (`type="info"`)** — *Default / Brand Purple*
  Use for general notes, beta/early access alerts, or platform context.
  ```mdx
  <Callout type="info">
    **Early Access Note:** The Q2Labs CLI is currently in beta. Ensure your environment meets compliance standards before processing PHI.
  </Callout>
  ```

* **Tip (`type="tip"`)** — *Brand Green*
  Use for helpful hints, shortcuts, and recommended practices.
  ```mdx
  <Callout type="tip">
    **Pro Tip:** You can export quantitative summaries directly to your local vault.
  </Callout>
  ```

* **Warning (`type="warning"`)** — *Brand Gold*
  Use for prerequisites, requirements, or non-destructive warnings.
  ```mdx
  <Callout type="warning">
    Ensure outbound port 443 is open for encrypted telemetry sync.
  </Callout>
  ```

* **Danger (`type="danger"`)** — *Crimson Red*
  Use for data loss risks, token revocations, or critical compliance alerts.
  ```mdx
  <Callout type="danger">
    Resetting vault keys will immediately invalidate all active researcher sessions.
  </Callout>
  ```

---

### 4. Code Blocks & Tabs

* **Standard Code Blocks:** Always specify the syntax language.
  ````markdown
  ```bash
  npm install @q2labs/cli
  ```
  ````

* **Multi-language Tabs:** Use `<CodeTabs>` and `<Tab>` for multi-environment commands.
  ```mdx
  <CodeTabs>
    <Tab label="npm">
      ```bash
      npm i @q2labs/cli
      ```
    </Tab>
    <Tab label="pnpm">
      ```bash
      pnpm add @q2labs/cli
      ```
    </Tab>
  </CodeTabs>
  ```

---

### 5. Writing Style Rules
* **No Emojis:** Avoid raw emojis in headings, bullet points, or callouts to keep an enterprise, professional appearance.
* **Direct & Action-Oriented:** Start steps with verbs (*"Configure"*, *"Run"*, *"Verify"*).
* **Healthcare Compliance:** Capitalize compliance terms correctly (e.g., `PHI`, `HIPAA`, `GDPR`, `Vault`).
```
