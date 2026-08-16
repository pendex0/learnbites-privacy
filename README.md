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

The policy has to keep matching what the app actually does. **A change to the way questions travel is
a change to this file, in the same week — not afterwards.** The published policy is a compliance
document for a children's app, so a gap between what it says and what the app does is not cosmetic.

The proxy landed in August 2026 and this file was rewritten for it: questions now go phone → a server
the developer runs → Anthropic, and the policy describes both hops, what the middle one logs, and
what it deliberately does not. Two things in it are load-bearing and should survive any future edit:

- **It must not claim or imply that the data stays in the EU.** The middle server is in Frankfurt,
  but Anthropic processes requests in whichever region it chooses. Saying "Frankfurt" without saying
  what it does *not* mean turns an accurate document into a false promise in the damaging direction.
- **The IP address is recorded on failed authentication only**, and the policy says so. That is
  enforced in the proxy by two separate log templates rather than by a conditional, so it stays true.
