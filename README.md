# FIFA World Cup 2026 — My Prediction

A self-contained, single-file interactive bracket predictor for the **FIFA World Cup 2026**, hosted at [shazmoghaddam.github.io/wc2026](https://shazmoghaddam.github.io/wc2026).

Pick your winners through every round — Round of 32, Round of 16, Quarter-finals, Semi-finals, the Final, and the 3rd place play-off — and share your predictions with friends.

---

## Features

### Bracket Table
- Full 32-team knockout bracket with predicted Round of 32 matchups based on group-stage favourites
- Click any team to advance them through each round
- Match dates, kick-off times, and venue shown for every fixture
- Time zone toggle: **ET · BST · CET · Local**
- Connector lines linking rounds visually
- Progress counter: **X / 32 picks made**
- **Full** and **Split** view toggle (Split = left/right bracket panels, each independently scrollable — ideal for larger screens)
- Undo last pick
- Reset all picks (two-tap confirmation)

### Groups Tab
- All 12 groups with team names, flags, and predicted rankings
- Colour-coded group leaders and runners-up

### My Champion Tab
- Hero card showing your predicted champion with flag and name
- Full journey breakdown: every round result, finalists, 3rd place
- Compare your predictions against real results once the tournament begins (Jun 28, 2026)

### Halftime Quiz
- 188 World Cup trivia questions across History, Records, Players, Hosts, Moments, and more
- Fully randomised — no category filters, fresh set every time
- 20 questions per round, instant answer reveal with educational feedback
- Letter grades (A+ → D) with colour coding
- Personal best score tracked locally

### Export
- One-click **Save as PNG** — exports the full page (header, bracket, all picks) as a high-resolution image
- Watermarked with site attribution

### Share
- Pre-written post text (champion, finalists, picks count) — copy and paste directly into any social platform
- Direct links: WhatsApp, X / Twitter, LinkedIn, Instagram, TikTok
- Full bracket link (encoded URL) for sharing your exact picks with friends

### UX Details
- **Dark mode** — full `prefers-color-scheme: dark` support
- **Fully responsive** — desktop (full bracket), tablet (compressed), mobile (accordion per round)
- Name and country inputs (session-only — not persisted between visits)
- Searchable country dropdown with flag display
- Picks persist in `localStorage` between sessions; name/country do not
- Inline SVG favicon, Open Graph and Twitter Card meta tags

---

## Tech Stack

| Layer | Detail |
|---|---|
| Language | Vanilla HTML, CSS, JavaScript — no build step, no framework |
| Rendering | All UI built and updated in plain DOM JS |
| State | In-memory JS objects; picks persisted via `localStorage` |
| Styling | Custom CSS with CSS variables, dark mode, and responsive breakpoints |
| Export | [html2canvas 1.4.1](https://html2canvas.hertzen.com/) (loaded on demand from cdnjs) |
| Hosting | GitHub Pages — single static file |
| External data | Match schedule and venues from the [Official FIFA World Cup 2026 website](https://www.fifa.com/en/tournaments/mens/worldcup/canadamexicousa2026) |

No npm, no bundler, no dependencies at runtime. The entire app is one `.html` file (~153 KB).

---

## Usage

### Run locally
Download `FIFA_World_Cup_2026_-_My_Prediction_fixed.html` and open it in any modern browser. All features work offline except the PNG export (which loads html2canvas from a CDN on demand).

### Deploy to GitHub Pages
1. Rename the file to `index.html`
2. Push to a GitHub repository
3. Enable GitHub Pages (Settings → Pages → Deploy from branch)
4. Visit `https://yourusername.github.io/wc2026`

The share URL and bracket link will work correctly once deployed.

---

## Data Sources

- Match schedule, venues, and kick-off times: [FIFA World Cup 2026 official website](https://www.fifa.com/en/tournaments/mens/worldcup/canadamexicousa2026)
- Group-stage predicted matchups based on published group compositions
- Quiz questions: original research, verified against official FIFA records

---

## Roadmap / Known Limitations

- Round of 32 matchups are **predicted** based on group-stage favourites — actual confirmed opponents will be known after Jun 27, 2026
- Real Results tab will be populated once the knockout stage begins (Jun 28, 2026)
- Social share preview cards show the static site preview image; personalised OG images per bracket are not possible with a static file (no server)

---

## License

See [LICENSE](LICENSE).

---

## Author

**Shaz Moghaddam** · London  
[shazmoghaddam.github.io](https://shazmoghaddam.github.io/) · [LinkedIn](https://www.linkedin.com/in/shazmoghaddam/) · [GitHub](https://github.com/ShazMoghaddam)
