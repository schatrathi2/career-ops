# /eval — Evaluate Only (No CV/PDF)

Run the full auto-pipeline for the job description or URL that follows this command, but **skip CV and PDF generation entirely**.

Usage: `/eval [JD text or URL]`

## What this does

Execute Steps 0, 1, 2, 4, and 5 from `modes/auto-pipeline.md` — everything except Step 3 (PDF generation).

### Step 0 — Extract JD
Same as auto-pipeline: Playwright → WebFetch → WebSearch → ask user.

### Step 1 — Evaluate (Blocks A–G)
Full evaluation per `modes/oferta.md`.

### Step 2 — Save Report
Save to `reports/{###}-{company-slug}-{YYYY-MM-DD}.md` with Block G and `**Legitimacy:**` header. No PDF column needed — mark PDF as ❌.

### Step 3 — SKIP
Do NOT generate a CV or PDF. Do not read `modes/pdf.md` or `modes/latex.md`.

### Step 4 — Draft Application Answers (only if score >= 4.5)
Same as auto-pipeline Step 4.

### Step 5 — Update Tracker
Same as auto-pipeline Step 5. Mark PDF column as ❌.
