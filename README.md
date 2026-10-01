a one-stop web app for college students. Enter your profile once, and Student Buddy checks which events, internships, perks and courses you qualify for, with links and registration guides.

**Live demo:** _add your link here after deploying_

---

## The problem

Students miss opportunities because information is scattered across dozens of websites, and it is hard to tell whether you are even eligible before you spend time registering. Student Buddy brings it into one place and does the eligibility check for you.
A
## Features

| Slide | What it does |
|---|---|
| **Profile** | Enter age, gender, college year, branch and city. Saved in your browser. |
| **Events** | Hackathons, meet-ups, marathons and sports fests. Each is marked Eligible or Not eligible with the reason, eligible ones first. Includes the official link and a step-by-step "How to register" guide. |
| **Internships** | Filter by Government or Private. Results in your city and remote roles come first, checked against your year and branch. Links to apply. |
| **Study abroad** | Documents checklist, where to live, how to survive and save money, student ID benefits, and study help. |
| **Perks** | Student ID discounts and free tools (ISIC, GitHub Student Developer Pack, Spotify, Canva and more), filterable by category, with links. |
| **Learn** | Free and paid courses (CS50, NPTEL, SWAYAM, Coursera and more) with duration, requirements and certificate details. |

## How eligibility works

Each event or internship has simple rules: an age range, allowed gender, allowed college years and allowed branches (internships use a minimum year and branches). The app compares your profile against these rules.

- If everything matches, it shows **Eligible**.
- If something fails, it shows **Not eligible** and lists the reasons.
- Eligible items are sorted to the top.

## Tech

- Plain HTML, CSS and JavaScript in a single file (`index.html`)
- No framework, no build step, no backend
- Google Fonts (Bricolage Grotesque) with system-font fallback
- Profile saved with `localStorage`
- Responsive, with light and dark mode and keyboard focus styles

## Run it locally

1. Download `index.html`.
2. Double-click it to open in your browser.

That is all. No installation needed.

## Deploy for free

**Netlify:** go to app.netlify.com/drop and drag `index.html` in.

**GitHub Pages:**
1. Create a repository and upload `index.html`.
2. Open **Settings → Pages**.
3. Set the source to your main branch and save.

## Edit the data

All listings live near the top of the `<script>` section as JavaScript arrays: `events`, `interns`, `abroad`, `perks` and `courses`.

Example event entry:

```js
{
  n: "Event name",
  t: "Hackathon",              // Hackathon, Meet-up, Marathon, Sports fest
  o: "Organiser",
  age: [17, 30],               // min and max age
  g: "all",                    // "all" or "Female"
  y: [1, 2, 3, 4],             // allowed college years
  b: "all",                    // "all" or ["CSE", "IT"]
  mode: "Online, 48 hours",
  url: "https://example.com",
  how: ["Step one", "Step two"]
}
```

## Important notes

- The events and internships are **sample listings** that demonstrate the matching logic. Always confirm dates, eligibility and fees on the official website before registering.
- Perk and course details change often. Each card links to the official page.
- Profile data stays in the user's own browser. Nothing is sent to a server.

## Roadmap

- Load listings live from a Google Sheet, Supabase or Firebase
- Real sign-in so profiles sync across devices
- Let organisers submit events through a form
- Saved and bookmarked items, and deadline reminders
- Search by city for events as well as internships
- Hindi and regional-language support

## Contributing

Found a wrong link or a new opportunity? Open an issue or send a pull request with the updated entry.

## Team

_Add your team name and members here._

## Licence

MIT. Free to use and modify.
