# Eladio Transport: interactive prototype

A bilingual (Spanish first, English toggle), mobile-first demo of a simple ride-coordination tool for Eladio's trusted driver service in Punta Hermosa, Lima. It exists to gather Eladio's feedback, not to run the business.

**Everything is sample data. Nothing is connected to WhatsApp, a database, payments or GPS. Do not enter real customer or children's data.**

## Files

The whole site is one file: `index.html` (HTML, CSS and JavaScript inline, no build step, no frameworks, no API keys). The only external request is the optional Google Fonts stylesheet; if it fails, system fonts are used.

## Publish on GitHub Pages

1. Create a new **public** repository on GitHub (for example `eladio-transport`).
2. Upload `index.html` (and this `README.md`) to the root of the `main` branch: **Add file > Upload files > Commit changes**.
3. Go to **Settings > Pages**.
4. Under **Build and deployment**, choose **Source: Deploy from a branch**, then **Branch: `main`** and folder **`/ (root)`**. Click **Save**.
5. Wait a minute or two. The site appears at `https://USERNAME.github.io/REPOSITORY/`.
6. Send that link to Eladio by WhatsApp. It works on any phone browser.

All links are relative, so the site works inside a repository subfolder. To preview locally, just open `index.html` in a browser.

## What works in this demo

- [x] Spanish / English toggle (Spanish by default; the choice is remembered on that device)
- [x] Intro page addressed to Eladio, with "how it works", the checklist below, and three feedback questions that open WhatsApp with his answers pre-filled
- [x] Role switcher: Eladio (manager), driver, family. Clearly labeled as **not** a login
- [x] Manager workspace: on a computer, three panes (rides needing action on the left, schedule in the middle, ride details on the right); on a phone, a bottom tab bar (Rides, Schedule, Drivers, WhatsApp) with details in a slide-up sheet
- [x] Manager: counts for requests to review, rides today, rides without a driver, and unpaid rides; a "needs your attention" list; ride lists by status
- [x] Manager: review and edit a request, enter the fare in S/, approve, assign or reassign a driver, cancel
- [x] Day schedule with one row per driver plus a "no driver" row; on a computer, drag a ride to another driver's row to reassign it (blocks are drawn as 1 hour for display only)
- [x] Week view, previous/next/today navigation; sample rides are generated around the current date
- [x] Driver roster with manually set availability
- [x] Simulated WhatsApp inbox: paste (or pick) a message, get a draft. Simple keyword matching only; anything not found clearly is left blank and marked "Check" rather than guessed
- [x] WhatsApp-ready messages per ride status, in Spanish or English, with **Copy** and **Open in WhatsApp** (a normal `wa.me` link; you choose the chat and press send)
- [x] Driver: today / upcoming / recent rides, accept or decline, arrived, passenger on board, completed; Google Maps and Waze links
- [x] Family: a four-step booking card (route, date and time, who's riding, review) with sample saved places and a swap button; a "next ride" card showing the trusted driver, car and fare once confirmed; "Message Eladio" links. States that a request is not confirmed until Eladio approves it
- [x] Paid / unpaid marking (cash, Yape, Plin or transfer happen outside the app)
- [x] Changes saved in this browser only (`localStorage`); **Reset demo** restores the sample data

## What is not connected yet

- [ ] Real accounts, passwords or permissions (anyone with the link can see every view)
- [ ] Reading or sending WhatsApp messages automatically
- [ ] Shared data between phones (each phone has its own copy)
- [ ] Schedule-conflict checking between a driver's rides
- [ ] Live GPS, route or travel-time calculation, or price suggestions
- [ ] Payments, payouts or financial reports
- [ ] Privacy notices, backups, audit trail, or protections for minors' data

## Later phases (design notes, not built)

- Shared backend with real role-based accounts and server-side authorization.
- Conflict checks using realistic ride durations and buffers; recurring school rides.
- Official WhatsApp Business Platform for incoming messages and outbound templates. This is different from the regular WhatsApp and WhatsApp Business apps, depends on Eladio's number and account, requires opt-in and approved templates, has per-conversation fees, and cannot read old chat history.
- Map-based distance, tolls and pricing suggestions (would need a paid maps API).
- Authorized guardian contacts and pickup/drop-off confirmations for minors.
- Payment and payout reporting, cancellation and no-show policies.
- Production hosting, backups and lawful data handling under Peru's personal data protection law.

Cost approach: keep recurring costs near zero until a feature proves its value. GitHub Pages hosting for this demo is free; future production pieces (backend, WhatsApp Platform, maps) will likely carry some cost.

## Self-review performed

Automated browser checks covered: language switch (all three views have no leftover Spanish UI text in English), role switch, family booking creation, WhatsApp draft creation from all four samples (including the deliberately vague one, which leaves pickup, time and passengers blank), manager approval with fare and driver assignment, Spanish and English confirmation messages, paid/unpaid toggle, calendar week/day toggle and navigation, the four-step family booking (validation, saved places, swap, passenger stepper, edit from summary), the full driver flow (accept, arrived, on board, completed), driver decline returning the ride to Eladio, availability toggle, Google Maps/Waze/WhatsApp link generation, local saving and reset, with no JavaScript errors. Screens were checked at 390 px (phone) and 1440 px (desktop), and timeline drag-and-drop was tested in Chromium.
