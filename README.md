# Scam Check

Paste a suspicious SMS, WhatsApp message, link, or a screenshot. **Gemma 4** (through the Gemini API) tells you whether it looks like a scam, why, and what to do next, in Hinglish, English or Hindi.

Built at **Hacktoberfest Hack Day Noida x NIAT-NIU** (31 Oct 2026).

## The problem

Fake KYC alerts, UPI "collect" requests, courier fee messages and job-task scams reach people in India every day. Most victims decide in a few seconds, with no one to ask. Scam Check gives them a quick second opinion in their own language.

## What it does

- Reads text **and** screenshots (Gemma 4 is multimodal).
- Gives a verdict (safe / suspicious / scam), a 0-100 risk score, the scam type, red flags and safe next steps.
- Runs an instant local link check (shortened links, IP addresses, odd domain endings, fake bank or brand names) before the AI answers.
- Answers in Hinglish, English or Hindi.
- Highlights the suspicious words inside the original message.
- One tap to copy the report or send a ready-made warning to family on WhatsApp.
- Paste (Ctrl+V) or drag-drop a screenshot; Ctrl+Enter to check.
- Shows the India cybercrime helpline (1930) and cybercrime.gov.in when the result is not safe.

## Run it

No install needed. It is a single HTML file.

1. Get a free API key from [Google AI Studio](https://aistudio.google.com/apikey).
2. Open `index.html` in your browser.
3. Paste the key, paste a message (or try a sample), and press **Check this message**.

Your key is stored only in your browser (`localStorage`) and is sent only to Google. Never commit it to the repo.

## Tech

- Plain HTML, CSS and JavaScript, no build step.
- Model: `gemma-4-26b-a4b-it` (default) or `gemma-4-31b-it`, called through the Gemini API `generateContent` endpoint.
- The model is asked for strict JSON, which is parsed and rendered with `textContent` so model output can never inject HTML.

## Limits

This is an AI opinion, not proof. Always confirm money or OTP requests by calling your bank on its official number.

## Ideas to contribute

- Add more languages (Marathi, Tamil, Bengali...).
- Add more sample scams and better local link rules.
- Save a history of checked messages.
- Make a browser extension or a WhatsApp bot version.

PRs are welcome.

## License

MIT
