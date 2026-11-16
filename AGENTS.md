# Project Rules: Energy Transition Report

## 1. The Goal
* Build a report about India's energy transition based on McKinsey's physical challenges.
* Show how Energy Group's infrastructure turns these challenges into a business advantage.

## 2. The Structure
* **Format:** A chain of Questions and Answers formatted as a continuous story, grouped into 8 Chapters. DO NOT use "Parts" (e.g., Runway, Core, Payoff) in the text itself.
* **The chapter and question list lives in `STORYLINE.md`.** Do not repeat question numbers here; they shift as questions merge or split.
* **The last chapter needs TWO VERSIONS:**
  * **Version A (General Audience):** Covers the remaining sectors and ends with a strong national conclusion.
  * **Version B (Energy Group Edition):** Covers the remaining sectors and moves into the Energy Group Opportunity payoff.
* **Sector answers follow the same layout every time:**
  1. A short opening riddle or game that sets up the sector.
  2. **Where the carbon emissions come from:** the sub-sources, with numbers (a table is fine).
  3. **The Beautiful Solutions:** what can replace each source, with one line on why they come in that order.
  4. **Look at Our Progress!:** what India has already built or achieved. Add a progress-against-targets line or table where a real number exists.
  5. **The Reality Check:** the physical challenge behind each solution.
  6. **A closing takeaway** that ends on the hook into the next sector.

## 3. The Audience and Tone
* **Audience:** An Indian layman.
* **Language:** Very simple, 5th-standard level English. Short sentences. Everyday words. This applies to the report AND the chat with the user.
* **Persona:** The Curious Detective (Feynman style): playful, logical, relies on simple thought experiments, highly conversational, and speaks directly to the reader like a friend over tea.
* **Tone:** Like a good, warm school teacher explaining something to a friend.

## 4. Writing Rules
* **Hooks:** Every answer must end with a hook leading to the next question.
* **Examples:** Use lots of everyday examples.
* **No Meta-Talk:** Never talk about the report itself (e.g., do not say "as we will see later").
* **No AI Dashes:** Strictly avoid using typical AI-style dashes (—). Use natural human punctuation like commas, periods, or colons to ensure the report does not look AI-generated.
* **Vocabulary Consistency (Human-Like Voice):**
  * Never use the word **"carbon"** on its own. Always use **"carbon dioxide"** (when referring to the gas) or **"carbon emissions"** (when referring to pollution shares).
  * Never use the words **"atmosphere"** or **"sky"**. Always use **"air"** consistently.
  * Always use **"giant home"** or **"Earth"** instead of "planet."
  * Always refer to electricity transmission losses as **"wire leaks"** or **"power leaking in our wires."**
  * Always refer to electricity capacity as **"power machines"** or **"clean machines."**
* **Formatting:** Use bullets only for lists. Put the main point in bold first, then explain.
* **Sourcing:** Put one italic line at the bottom of each answer for the source. Be honest if a number is a guess.

## 5. Process Rules
* **Step-by-Step:** Write one chapter and one question at a time.
* **Draft First:** Always draft the answer in the chat first.
* **Strict Approval Gate:** NEVER save a file or move to the next question until the user has explicitly said "yes", "approved", or otherwise confirmed they are happy with the current draft. Do not assume approval.
* **One Master File:** All approved text goes into `draft/revised_draft.md`. The files in `archive/` are read-only: use them for facts and old drafts, never edit them.
* **Check for Contradictions:** Always actively verify the content against the referenced resources to ensure there are no contradictions or factual errors before finalizing a draft.

## 6. Tool Rules
* **Web Search:** Must use PowerShell for online searches (`Invoke-WebRequest -Uri <url> -UseBasicParsing -TimeoutSec 30`). Do NOT use default web search tools. `cea.nic.in` often drops the first connection: retry 2 to 3 times.
* **PDFs:** Must use Python scripts (`pypdf`) to read PDF files. Source PDFs are not stored in the folder; download them on demand from the links in `SOURCES.md`.

## 7. Where Things Are
* `STORYLINE.md`: chapters, questions, hooks, sources, and what is left to write.
* `draft/revised_draft.md`: the master text.
* `reference/`: the research notes. Start at `reference/00-INDEX.md`.
* `design/`: the look of the final PDF (design brief, layout plan, colours, chart data, logo).
* `archive/`: older versions of every question, kept for facts. Read-only.
* `SOURCES.md`: links to the main source reports.
