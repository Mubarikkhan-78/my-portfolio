# Mubarik Khan — Personal Portfolio

A responsive, mobile-friendly personal portfolio for Mubarik Khan, a first-year
B.Tech student at JECRC University, Jaipur, Rajasthan. Blue-and-white theme,
animated sections, clear navigation, and seven pages.

## Pages

| Path | Page |
| --- | --- |
| `/` | Home — introduction, photo, career direction |
| `/about` | About Me — background and career goals |
| `/education` | Education — JECRC University, Jaipur |
| `/skills` | Skills — technical skills and learning focus |
| `/projects` | Projects — placeholders for future work |
| `/certifications` | Certifications & Achievements |
| `/contact` | Contact — email, GitHub, LinkedIn |

GitHub and LinkedIn links appear in the header, on the home page, and in the footer.

## Run it locally

You need Node.js 20.19 or newer (Node 22 recommended).

```sh
npm install
npm run dev
```

Open the printed address (usually http://localhost:8080).

Other commands:

```sh
npm run build     # production build
npm run preview   # serve the production build
npm run lint      # code checks
npm run test      # unit tests
npm run format    # code formatting
```

`bun install` / `bun run dev` also work — `bun.lock` is included.

## Project structure

```text
src/
  routes/            one file per page (about.tsx, contact.tsx, ...)
  components/
    portfolio/       pages.tsx (all page content), shell.tsx (nav + footer),
                     profile.tsx (editable personal details)
    ui/              reusable UI building blocks
  assets/            photo reference used by the Home page
  styles.css         all colours, layout and animations (Tailwind CSS v4)
public/
  mubarik-khan.jpg   your photo, served at /mubarik-khan.jpg
```

## Your photo

`src/assets/mubarik-khan.jpg.asset.json` points to `/mubarik-khan.jpg`, so the
photo in `public/` is shown on the Home page and the About page. To replace it,
save a new photo over `public/mubarik-khan.jpg` (keep the same filename) — no
code change needed.

## Editing your details

Introduction, about text, career goals, skills, email, GitHub and LinkedIn are
editable from the **Edit profile** button in the footer. Those edits last for the
current visit only — to make them permanent, change the values in
`src/components/portfolio/profile.tsx`.

## Built with

- TanStack Start (React 19 + Vite)
- TypeScript
- Tailwind CSS v4
- shadcn/ui components, Lucide icons
- Framer-free CSS animations

## Ownership

This project was built with [Lovable](https://lovable.dev). The code is yours:
push it to your own repository and keep working there, or connect the repository
to Lovable so changes sync back into the editor.
