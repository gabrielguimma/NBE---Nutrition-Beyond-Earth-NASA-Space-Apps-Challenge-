# NBE — Nutrition Beyond Earth

Health monitoring for astronauts, built from nutrition outward.
NASA Space Apps Challenge 2026 · Challenge: *Create Health Monitoring Software for Astronauts on Space Missions* · Team NBE.

> DEMO — test build with sample data only. Not a medical device and not an official NASA product.
> NBE supports, not replaces, the flight surgeon.

**Team NBE:** Gabriel Guimarães · Daniel Marcos · Lucas Pires

**Demo video (30 s):** (https://youtu.be/nSZbeIifT_A)

## What it does
- **Two-minute check-in:** meals from the NASA Artemis II crew menu (nutrients from USDA FoodData Central and TACO), fluids, exercise, sleep, mood, fatigue (Samn-Perelli) and a body check (resting heart rate, symptoms, warning signs).
- **Crew Readiness Score (0–100):** transparent, weighted rules based on NASA-STD-3001 and JSC-67378.
- **Risk Radar:** six risk signals (bone, body mass, hydration, mind, immune, heart) with OK / Watch / Act states. Risk signals, never diagnosis.
- **Act Now:** a concrete on-board action for every signal.
- **Ground Link:** structured daily records (CSV / JSON) tagged with NASA DONKI space-weather events; messages from Houston.
- **Ground Control:** whole-crew overview for the flight surgeon and ground team.
- **Food Stores:** ship-wide inventory that counts itself down from the check-ins, with days of supply and resupply planning.
- **Checked against NASA flight data:** the rules are compared with published ISS results (Zwart et al. 2014; Smith et al. 2012).

## How to try it
1. Open the live link (or download `index.html` and open it in any browser — it also works offline).
2. Press **Space** (or tap) on the launch screen.
3. Sign in with a demo PIN: seat 1 → `111`, seat 2 → `222` … seat 6 → `666`. **Ground Control** (seat 7) opens without a PIN.
4. Use **Test → Skip a day / Skip 7 days** to move the mission clock forward. **Reset demo data** (About) restores Day 42.

Data stays in your browser (localStorage). The PINs are a privacy screen for the demo, not real security.

## Tech
One HTML file (`index.html`) with the CSS and JavaScript written inside it: no server and no build step. That is why GitHub lists the repository as 100% HTML. SVG charts drawn in code; Three.js (r128, CDN) for the 3D body hologram; NASA DONKI API for space weather (cached sample when offline).

## Use of AI
Health logic uses no AI: every score and signal follows rules stored in `NBE_CONFIG`, each with its source.
Claude (Anthropic) assisted with programming the app's backend and with automated tests of the screens and calculations; ChatGPT (OpenAI) helped organize information and review texts; Figma was used for the screen design. The NBE logo is AI-generated. The demo video's narration is an AI-generated voice (ElevenLabs), from a script written by the team.

## Sources
All references (NASA standards, NASA technical reports, USDA, TACO, analog studies) are listed with links in the app's **About → References** page.

## Team
Three nutrition undergraduates from Brazil; one also holds a Physical Education degree and studies systems analysis and development.

## License
MIT — see `LICENSE`. Third-party data and references keep their own terms.

## Two builds
- `index.html` — readable source (use this to study or edit the code).
- `index-protected.html` — same app with the JavaScript packed so it is not readable in "View Source"; rename it to `index.html` on GitHub Pages if you prefer to publish the packed build. Note: any browser app can still be recovered by a determined user — packing only discourages casual copying, it is not true encryption.

## Authorship and license
Team NBE — Gabriel Guimarães, Daniel Marcos, Lucas Pires.
© 2026 Team NBE. All rights reserved. See `LICENSE` — do not copy or redistribute without permission.
