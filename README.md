# LIFE MODE — MVP 0.1

Original browser-based educational life-skills simulator (18+ testing prototype).

**Status:** working static MVP; not yet publicly deployed. No backend, login, third-party assets or automatic data collection. User progress stays in browser localStorage; survey responses can be copied/exported voluntarily.

## MVP features

- RU / EN / IT interface
- Interactive four-room house
- Eight-field self-assessment life map
- Three practice scenarios with three choices each
- Real-world action prompts, symbolic XP
- Future-self goal/intention and optional affirmation
- Three-question voluntary feedback form

## Cloudflare Pages: connect with GitHub

1. Create a new **private** GitHub repository called `life-mode-mvp` under your account; don't initialize it with a README if pushing locally.
2. Upload or push this repo contents, including `public/index.html`.
3. In Cloudflare, open **Workers & Pages → Create application → Pages → Import an existing Git repository**.
4. Authorize GitHub and select `<your GitHub account>/life-mode-mvp`.
5. Set:

   | Setting | Value |
   | --- | --- |
   | Framework preset | None |
   | Production branch | `main` |
   | Build command | (leave empty) |
   | Build output directory | `public` |
   | Root directory | (leave empty / repository root) |

6. Deploy and verify the assigned `*.pages.dev` domain. Future commits to `main` will deploy automatically.

**Important:** Select Git integration **when creating** the Cloudflare Pages project. A Pages Direct Upload project cannot later be converted to Git integration. This package doesn't need NPM or a build system.

### Push from a local terminal (after creating an empty repository)

```bash
git init
git branch -M main
git add .
git commit -m "Initial LIFE MODE MVP 0.1"
git remote add origin https://github.com/Pryshvitsyn/life-mode-mvp.git
git push -u origin main
```

## Feedback and data

This is an exploratory self-reflection game, **not clinical guidance or psychological assessment**. Scores do not represent personal value or diagnostic indicators. Do not enter sensitive health data or identifying information. Published site is accessible to anyone with the URL even if GitHub repo is private. `robots.txt` discourages indexing, **not a security control**. To limit access during a closed test, add a real authentication / access layer, such as Cloudflare Access.

## Next steps

Add feedback endpoint and separate participant consent before scaling recruitment; validate user retention, navigation, and whether participants actually perform real-world tasks. Integrate original Avatar Studio assets only after licensing review and first test results.
