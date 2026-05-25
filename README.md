# SLAN Lead Capture Form

Static HTML form for SLAN Finance lead capture. Posts to the SLAN CRM API which fires an immediate Retell AI callback.

## Stack
- Plain HTML / CSS / JS, no build step
- Deployed on Vercel: https://slan-form.vercel.app

## What it does
1. Captures: name, AU mobile, email, loan purpose, timeline
2. Normalizes phone to E.164 (+61...)
3. POSTs JSON to `https://slan-crm.vercel.app/api/leads`
4. CRM fires a Retell call to the lead within ~5 seconds

## Editing
- `index.html` — single-file form (HTML, inline CSS, inline JS)
- `vercel.json` — Vercel static-site config

Change the CRM endpoint at the top of the `<script>` tag:
```js
const WEBHOOK_URL = "https://slan-crm.vercel.app/api/leads";
```

Full stack docs in the [slan-lead-qualification-CRM](https://github.com/arjun181105/slan-lead-qualification-CRM) repo.
