# learnbites-privacy

The privacy policy for the **LearnBites** Android app (`dev.dimitrovd.learnbites`), published as a
plain page so it has a stable public URL.

- **Live:** https://pendex0.github.io/learnbites-privacy/
- **Source:** `index.html` — one file, no build step, no dependencies.

## Why this is its own repository

Google Play requires every app to declare a privacy policy at an active, publicly accessible,
non-geofenced URL that is not a PDF and is not editable by visitors. The LearnBites source repository
is private, and GitHub Pages does not serve from a private repository on a free plan — so the policy
lives here instead, in the smallest public repository that satisfies the requirement.

The same URL is linked from inside the app, which Play also requires.

## Changing it

Edit `index.html`, update the "last updated" date in **both** language sections, and push to `main`.
Pages redeploys on its own.

The policy has to keep matching what the app actually does. The change already on the horizon is the
Anthropic call moving off the phone and behind a proxy — when that ships, the "where the data goes"
section is wrong until it is rewritten.
