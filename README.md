# The Unread Problem — What Did I Miss?

A privacy-first, purely browser-local web application that analyzes long, unread group conversations and extracts action items, decisions, and deadlines. Built for hackathons.

## Features

- **100% Local Processing:** No APIs, no backend, no data egress. Analyzes entirely via deterministic heuristics in your browser memory.
- **Eisenhower Matrix:** Automatically sorts extracted tasks into an urgency vs. importance grid.
- **Conflict Resolution:** Detects when a deadline is updated in a later message and flags the old message as superseded.
- **Evidence-Based:** Every extraction links directly back to the original source message to prevent AI hallucinations or parser misinterpretation.

## Stack

- React 18, Vite, TypeScript, Tailwind CSS, Vitest.

## Installation & Running Locally

Ensure you have Node.js (v18+) installed.

1. Install dependencies:
   \`npm install\`
2. Run development server:
   \`npm run dev\`
3. Run tests (Analyzer logic):
   \`npm run test\`
4. Build for production:
   \`npm run build\`

## Known Limitations

- Rule-based regex engines struggle with sarcasm, deep contextual slang, and severe typos.
- Timestamps currently do not resolve complex time zones natively without strict formatting.
- Large files (>10MB) might cause brief main-thread blocking since Web Workers are not utilized in this initial prototype.
