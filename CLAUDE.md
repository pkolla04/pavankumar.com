# Project: pavankumar.com

## Autonomy preferences

For this project only, operate autonomously on code and deployments. Default to acting without asking for confirmation on:

- Committing changes to the working branch
- Pushing to the remote (respecting the required `claude/*` branch naming from the session briefing)
- Creating pull requests
- Merging pull requests into `main`
- Triggering the GitHub Pages deploy workflow (implicit on merge to `main`)

**Always pause and ask the user** when the next step involves:

- Manual testing on a real device (mobile browser QA, cross-device rendering, touch interactions, visual/perf checks that require human eyes)
- Anything the user would need to verify in a live browser that Claude can't headlessly validate

When asking for test verification, state exactly what to check and where — e.g. "Pull up `pkolla04.github.io/pavankumar.com/` on your phone; confirm X, Y, Z."

## Other context

- Static site: Next.js (`output: "export"`) deployed to GitHub Pages via `.github/workflows/deploy.yml`.
- Lives at `https://pkolla04.github.io/pavankumar.com/` (custom domain `pavankumar.com` planned but DNS not yet live).
- Project-page `basePath` is wired through the `NEXT_PUBLIC_BASE_PATH` env var in the workflow; don't remove it until the custom domain is active.
