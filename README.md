# InsightStudio - GraphQL + Knowledge AI Workbench
A Local-First AI Workspace for Knowledge, Chat, and GraphQL Exploration

Three distinct value propositions:
- A simple personal knowledge base
- A local-first, context-aware AI chat
- A full GraphQL inspector and schema explorer

This combination makes it uniquely useful for:
- Developers working with APIs
- Students learning GraphQL and LLM prompting
- Anyone wanting a private, “no-backend” knowledge assistant
- People who want an AI that can ingest their structured knowledge, not just ad-hoc messages

InsightCanvas is an integrated, browser-native tool designed to streamline your workflow by unifying three core capabilities:

1. **Knowledge Base Manager** – Create, organize, import, and export your own knowledge cards.  
2. **Context-Aware AI Chat Assistant** – Provide selected knowledge as context to the AI and interact using your Groq API key.  
3. **GraphQL Inspector Console** – Test endpoints, manage headers and authentication, introspect schemas, and run queries with history tracking.

All data is stored locally via `localStorage`. No backend, no cloud storage, no external services beyond your configured APIs.

---

## Key Features

### Knowledge Base  
- Add, edit, delete, search, and tag knowledge cards.  
- Import/export cards as JSON for version control or sharing.  
- Dedicated left-pane knowledge browser in the Chat tab.  
- Select cards to feed directly as context into the assistant.

### AI Chat Assistant  
- Uses your Groq API key for fast LLM interactions.  
- Configure model, temperature, max tokens, and system prompt.  
- Streams responses in real time.  
- Includes context injection based on selected knowledge cards.

### GraphQL Inspector  
A complete GraphQL utility inside your browser:

- Configure endpoints, authentication, and custom headers.  
- Test connectivity and introspect schema types, queries, and mutations.  
- Build and execute queries with variables.  
- Auto-formatted responses with status indicators.  
- Query History with load + delete support.  
- Local configuration persistence.

---

## Technology Stack

- **Frontend:** Vanilla JavaScript + TailwindCSS  
- **Storage:** `localStorage` (no backend required)  
- **AI:** Groq API (user-provided key)  
- **Environment:** Fully client-side (works offline except for GraphQL/API calls)

---

## Installation

Clone the repository:

```bash
git clone https://github.com/benneberg/graphgl-llms.git
cd graphgl-llms
````

Open the application:

```
index.html
```

No build step is required.

---

## Usage

### 1. Knowledge Base

* Navigate to the **Knowledge** tab.
* Create cards, apply tags, or import/export a JSON file.
* Use cards later as AI chat context.

### 2. AI Chat

* Open **Settings** and enter your Groq API key. (Easy to change api calls in src to what ever required like openrouter, opaenai etc)
* Select a model from the automatic model list.
* Select cards from the left knowledge pane to inject their content as context.
* Start chatting.

### 3. GraphQL Inspector

* Enter your endpoint URL.
* Configure auth header type.
* Add custom or JSON headers.
* Test connection or run introspection.
* Build and execute queries.
* Manage query history.

---

## JSON Knowledge Cards

Included in this repository is a JSON file containing ready-to-use “Good to Know” cards.
Format:

```json
[
  {
    "id": "unique-id",
    "title": "Some Title",
    "tags": ["tag1", "tag2"],
    "content": "Any explanatory text you want."
  }
]
```

You can import this through the **Import JSON** button.

---

## Roadmap Ideas

* Multi-file knowledge collections
* Sync/export to GitHub Gists
* GraphQL autocomplete and schema-driven query generation
* Multi-assistant profiles
* Plugin architecture for specialized panels
* Offline packaged LLM support (local models)

---

## License

MIT License, allowing private and commercial use with attribution.

---

## Screenshots

(Might come later: screenshots or GIFs of:

* Knowledge Base
* AI Chat Window
* GraphQL Console
  )

---

# Contribution

Pull requests and issue reporting are welcome.

---

# Security Notice

InsightCanvas stores all settings, knowledge, and history **locally** in your browser.
API keys are never transmitted to any server other than the API endpoints you explicitly configure.

```

---
