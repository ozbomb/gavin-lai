# 🧠 AI Research Assistant: Design Document

## 🎯 The Goal
A "Human-in-the-loop" automated workflow that acts as a dedicated research assistant for your DBA.

## ⚙️ The Workflow (The "Pipeline")

### 1. The Sourcer (Input)
*   **Goal:** Scan diverse sources for new content.
*   **Sources:**
    *   Google Scholar (Keywords / Authors).
    *   **Email Alerts:** Google Scholar Alerts, Academia.edu, Newslwtters (IMAP Parser).
    *   Specific Domain Websites / Blogs.
    *   Social Media (Twitter/X, LinkedIn) for announcements.
    *   Podcasts / YouTube (Transcripts).
*   **Tech:** Python Scrapers, IMAP (Email), RSS Feeds.

### 💻 Infrastructure
*   **Platform:** Compatible with Mac/Windows/Linux.
*   **Storage:** Works directly with iCloud Drive / Obsidian Vaults on Mac.

### 2. The Filter (AI Analysis)
*   **Goal:** Remove noise. Identify "Promising" content.
*   **Criteria:**
    *   Topic relevance (Semantic similarity).
    *   Specific Authors / Institutions.
    *   Company / Industry mentions.
*   **Tech:** LLM (Gemini/GPT) to score relevance 1-10.

### 3. The Synthesizer (Salient Points)
*   **Goal:** Extract value without reading the whole thing.
*   **Output:** Bulleted summary of "Salient Points" (Methodology, Findings, Implications).
*   **Tech:** LLM Summarization.

### 4. The Archivist (Zotero)
*   **Goal:** Metadata management and PDF retrieval.
*   **Actions:**
    *   Find/Download PDF.
    *   Add to Zotero Library.
    *   Tag automatically.
*   **Tech:** Zotero API (`pyzotero`).

### 5. The Connector (Obsidian)
*   **Goal:** Integrate with your "Second Brain".
*   **Actions:**
    *   Create a new Note for the paper.
    *   **"Semantic Search":** Check existing Obsidian vault for related notes.
    *   **Propose Connections:** "This contradicts your note on X" or "This supports Y".
*   **Tech:** Local File Manipulation (Markdown), Vector Database (for semantic search of your vault).

### 6. The Reporter (Daily/Weekly Brief)
*   **Goal:** User Review.
*   **Output:** An email or Markdown dashboard showing:
    *   "3 High Priority Papers (Review Now)"
    *   "5 Industry Updates (FYI)"
    *   PROPOSE ACTION: "Add this to paper section 4?"

## 🚀 Implementation Stages

### Phase 1: The "Newsboy" (Sources & Summary)
*   Build a script that scans 1 source (e.g., Google Scholar) and emails a summary.

### Phase 2: The "Librarian" (Zotero Integration)
*   Connect the script to Zotero to save what it finds.

### Phase 3: The "Analyst" (Obsidian & Connections)
*   The most advanced part. Reading your local Obsidian vault to spot connections.
