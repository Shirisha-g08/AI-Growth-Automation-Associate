# VisitPrep

VisitPrep is a privacy-first healthcare appointment-preparation prototype. It turns a person's own rough notes into a structured, carefully bounded prompt they can review and optionally use with an AI assistant they trust.

## Try it

Open `index.html` in a current browser. No installation, account, API key, or build step is required. For consistent clipboard behavior, serve the folder locally:

```powershell
python -m http.server 8000
```

Then visit <http://localhost:8000>.

Use **Try a sample note**, select **Create my AI prompt**, and then try **Copy prompt**, **Download .txt**, and **Start over**. The sample is fictional and for demonstration only.

## What it does

- Accepts up to 4,000 characters of free-form visit notes.
- Generates a reusable prompt that asks an AI to organize the notes into concerns, user-provided timeline details, neutral questions, and details to remember.
- Explicitly tells the AI not to diagnose, recommend treatment, change medication, invent facts, or follow instructions embedded in the notes.
- Lets the user copy or download the prompt; it never submits information to a model.
- Works without dependencies, external font requests, or a backend. Notes live only in the current page and are cleared when it is closed or reset.

## AI use and project approach

An AI assistant was used to brainstorm the user problem, shape the prompt constraints and user flow, and implement the prototype. The core project feature is itself a prompt-building workflow: the user may take the generated prompt to an AI service of their choice, but this app does not call an AI model. The actual project prompts and iterations are recorded in [PROMPTS.md](./PROMPTS.md).

The solution is intentionally not a symptom checker. It addresses a practical communication problem—remembering what to discuss—while avoiding automated clinical judgments and external processing of sensitive notes.

## Safety and privacy

This is an educational prototype, not a medical device or source of medical advice. It does not store or transmit notes in the app. A user who chooses to paste a prompt into another service should review that service's data practices and avoid sharing information they do not want processed there. For urgent concerns, contact a local emergency service or healthcare professional.

## Project files

- `index.html` — accessible, responsive interface
- `styles.css` — layout and visual design
- `app.js` — local prompt generation, copy, download, and reset interactions
- [PROMPTS.md](./PROMPTS.md) — prompt documentation and iterations
- [VIDEO_SCRIPT.md](./VIDEO_SCRIPT.md) — presentation script designed for a 2–3 minute recording

## Project link

This workspace contains the complete runnable project. It has not been published to a public hosting service; open the folder locally or upload it to a hosting provider to create a shareable public link.
