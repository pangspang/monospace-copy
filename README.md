# Monospace Copy - Minimal Prompt Viewer

Monospace is a clean, minimal, and content-focused single-page application designed to present and share text prompts, structured documentation, or markdown files. It provides an optimized reading experience with built-in dark mode support and a single-click copy mechanism to easily retrieve the raw text source.

---

## Core Features

### 1. Adaptive Interface (`index.html`)
- **System-Aware Theme Switching:** Seamlessly toggles between light and dark typography themes based on user operating system preferences (`@media (prefers-color-scheme: dark)`).
- **Responsive Typography Layout:** Focused around a 720px structural column container, optimal for reading multi-paragraph text or structured prompt frameworks.
- **Dynamic Clipboard Utility:** A dedicated custom interaction button allows users to instantaneously copy the entire raw layout content directly into their clipboard, complete with subtle visual success states (`Gekopieerd!`).
- **Markdown Architecture Parsing:** Leverages the `marked.min.js` rendering framework to convert raw text attributes into semantic structural headers (`<h1>`, `<h2>`), paragraph line breaks, and listed data objects.

### 2. Isolated Data Architecture (`monospace.js`)
- **Declarative Content Injection:** Decouples text assets and content management completely away from structural markup templates.
- **Preserved Format Encoding:** Preserves line-breaks, spacing parameters, and precise technical syntaxes flawlessly via clean JavaScript template strings.

---

## Data Format Strategy

The application references a standalone JavaScript file to feed content to the renderer. The document relies entirely on a single globally declared variable named `rawPromptMarkdown`.

### Content Configuration Example
To present custom content, encapsulate the structured layout format within backticks (`` ` ``) assigned directly to the `rawPromptMarkdown` string constant:

```javascript
// monospace.js
const rawPromptMarkdown = `# Your Primary Structural Header

## Sub-Section Focus
Detail your contextual descriptions or functional guidelines here.

* Bullet point consideration item 1
* Bullet point consideration item 2

---

### Technical Constraints or Scope
1. Ordered requirement overview
2. System rules or behavioral rules`;
