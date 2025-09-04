# MS-Copilot-Semantic-Index-API
Semantic Index is a tenant-wide knowledge map that powers Microsoft 365 Copilot.

**Background:** Semantic Index is the backbone of how Microsoft 365 Copilot grounds its answers in your enterprise data.

It takes all your organization’s content across SharePoint, OneDrive, Teams, Exchange, and more.
Instead of just keyword search, it builds a vectorized semantic index → so Copilot can understand meaning and not just text matches.
Example: If you ask, “Show me our Q4 financial forecasts”, Copilot doesn’t just search for the exact words, it finds related concepts, like “budget projections” or “revenue forecast”.

**How it works:**
Content ingestion → Copilot crawls M365 content (Word, Excel, PPT, PDF, Outlook, Teams).
Processing → Content is chunked into smaller pieces and vectorized (semantic embeddings).
Indexing → These embeddings are stored in the Semantic Index.
Querying → When you ask Copilot something, it queries the index → retrieves the most relevant context → grounds the LLM response.

**What Gets Indexed?**
File types: Word, Excel, PowerPoint, PDF, email, chats, calendars, and notes.
Limits:
File size: ≤ 512 MB (larger files are skipped for now).
Supported formats only (unsupported ones are skipped).
Granularity: Indexed at the content level (sections, slides, sheets) — not just the whole file.

**Security & Access Control**
Semantic Index respects permissions.
If you don’t have **read** access to a file/site Copilot won’t surface it for you.
Inherits Microsoft Graph’s security trimming model.

**Why It Matters**
Better grounding → Copilot answers are tied to your enterprise data.
Context-aware search → Goes beyond keyword search.
Productivity boost → Employees spend less time searching, more time doing.



Productivity boost → Employees spend less time searching, more time doing.
