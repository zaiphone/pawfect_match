
PawFect Match

A lifestyle quiz that uses Gemini AI to find your perfect pet breed — and links you straight to real adoption listings.
[🐾 Live Demo → pawfectmatch.click](https://pawfectmatch.click)

<img width="532" height="412" alt="Screenshot 2026-06-09 at 18 53 28" src="https://github.com/user-attachments/assets/f38580fa-e2e4-4743-aef3-40cf3631ee67" />

What it does

PawFect Match asks 13 questions about your lifestyle — living space, activity level, budget, allergies, hours at home, and more — then sends your answers to Gemini AI, which returns your top 10 breed matches ranked by compatibility percentage.

Each result includes:

Why the breed suits your lifestyle
Care difficulty and energy level
A direct link to real adoption listings on Petfinder filtered by your location and breed
There's also an optional Q14: enter a specific animal type and breed, and instead of the top-10 list you get a dedicated compatibility check — a 0–100 score, a verdict (Great / Good / Poor Match), reasons it works, any warnings, and a one-sentence recommendation. A "See My Top Matches Instead" button lets you switch to the normal results without re-doing the quiz.

Tech stack

Layer	Choice
Monorepo	pnpm workspaces
Frontend	React 19 + Vite, TypeScript, Tailwind CSS, shadcn/ui, Framer Motion
Routing	Wouter
Backend	Express 5, Node.js 24, TypeScript
AI	Google Gemini (gemini-2.5-flash) via @google/genai
State	React Context (no localStorage — memory only)


What I'd improve

Breed images — pull a photo of each matched breed from a public API (e.g. Dog CEO, The Cat API) so the results page is more visual
Save & share results — generate a shareable link or let users screenshot a results card
More animal types — the quiz is currently tuned toward dogs and cats; expanding prompts and Petfinder routing to cover rabbits, birds, and reptiles properly would broaden appeal
Smarter Petfinder links — use the Petfinder API directly to show live adoption counts per breed before the user clicks through
Quiz personalisation — let users weight what matters most to them (e.g. "shedding is a dealbreaker") so the AI ranking reflects their priorities more precisely
Persistent history — optionally save past quiz results to a user account so people can track how their preferences change over time
