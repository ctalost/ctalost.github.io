# Ishan Shaji — Developer Portfolio

Full source for Ishan Shaji’s React portfolio, including animated projects, responsive layouts, contact links, and automatically refreshing public GitHub activity.

Built with React, TypeScript, Vite, Tailwind CSS, Framer Motion, and Lucide icons.

## Upload to GitHub

1. Extract `ishan-shaji-portfolio-source.zip`.
2. Create a repository on GitHub, or open the repository you want to use.
3. Choose **Add file → Upload files**.
4. Upload the files and folders **inside** `ishan-shaji-portfolio`, so `package.json`, `index.html`, `src/`, and `public/` are at the repository root.
5. Commit the upload. Upload the extracted source files, rather than only the ZIP.

The archive excludes dependency folders, build output, Git history, and private Site hosting configuration.

## Run locally

Use Node.js 24 (specified in `.nvmrc`) and npm.

```sh
npm ci
npm run dev
```

Open the local URL printed by Vite.

## Build and preview

```sh
npm run build
npm run preview
```

Production files are generated in `dist/`. Vercel and Netlify can build the repository using the Vite preset, `npm run build`, and output directory `dist`.

## Edit the portfolio

- `src/main.tsx`: personal information, projects, contact links, and page sections.
- `src/styles.css`: styles, mobile layouts, and reduced-motion support.
- `src/github.ts`: public GitHub requests, types, refresh policy, and timestamps.
- `src/useGithub.ts`: automatic refresh, manual refresh, and error handling.
- `src/fonts.css` and `public/fonts/`: self-hosted typography.
- `public/argon-preview.png`: Argon-Bridge screenshot.
- `public/favicon.svg`: favicon.
- `index.html`: SEO and social metadata. Update `og:url` if you change the website address.

Featured projects are Argon-Bridge, RoastMyRoom, and MX1, linked to their public repositories. RoastMyRoom is labeled as an early project and MX1 as an experimental test build.

Contact links include GitHub, LinkedIn, Discord, and `ishanccj@gmail.com`.

GitHub data refreshes every five minutes while the page is visible. Manual refresh has a one-minute cooldown. The site keeps the last successful data visible during errors and respects API rate limits. Public GitHub events can be delayed. No API token or environment variables are required.

## Checks

```sh
npm test
npm run build
```

Tests cover GitHub loading, pagination, refresh scheduling, cooldown, and rate limits. The production build also checks TypeScript.

## Fonts

DM Sans, Manrope, and IBM Plex Mono are distributed under the SIL Open Font License. License files are included in `public/fonts/licenses/`.
