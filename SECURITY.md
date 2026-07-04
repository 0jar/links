# Security policy for Jarema's link-in-bio page

This is the source for my personal link-in-bio page on [https://jar.tf](https://jar.tf). It's a personal project and not a commercial product, there's no bug bounty either, but I do care about getting security issues fixed quickly and I'd rather hear about a problem from you than from my logs.

## Scope

In scope:

- The domain: jar.tf
- This repository, including:
  - All code inside the `components/`, `data/`, `pages/`, `scripts/` and `styles/` folders
  - Configuration files and middleware (`next.config.js`, `next-seo.config.js`, `proxy.js`)
  - The permanent and temporary shortlink functionality
- All files hosted publicly (the `public/` folder)

Out of scope:

- Third-party services the site integrates with but doesn't control. Please report those issues directly to their maintainers, but you can still notify me *after reporting upstream* so I could try to mitigate it in the meantime.
- Generic Next.js, React, or styled-components framework bugs with no site-specific exploit. Same as above, please report those upstream.
- Issues that only affect outdated forks and not applicable to the latest codebase in the `main` branch.
- Denial of service via brute-force traffic or rate-limit exhaustion against third-party APIs
- Anything that requires physical access to my devices or social engineering against me personally
- Missing security headers or best-practice suggestions with no clear demonstrated impact (open an issue for those instead)

Not security issues:

- Content disputes
- Broken links in my profile
- Anything that isn't a security vulnerability.

Open a normal issue for those.

## Supported versions

This is a personal site with a single rolling release, only the `main` branch is maintained. There are no version branches to track, and there's no expectation that older deployments stay patched, since the live site always reflects `main`.

## Reporting a vulnerability

Please don't open a public issue on Codeberg, GitHub, or GitLab for anything that could be actively exploited before a fix ships. Send a private email to me at [security@jarema.me](mailto:security@jarema.me) instead. My PGP key can be found at [https://keys.openpgp.org/vks/v1/by-fingerprint/D5A8DEAE823F6478185C39879BB802C53628AE75](https://keys.openpgp.org/vks/v1/by-fingerprint/D5A8DEAE823F6478185C39879BB802C53628AE75).

> **PGP key fingerprint:** `D5A8 DEAE 823F 6478 185C 3987 9BB8 02C5 3628 AE75`

Alternatively, contact me on Signal at `@jarema.26`.

Either way, please include:

- A description of the issue
- Steps to reproduce, or a proof of concept if you have one
- Your assessment of impact, if you have one

## Response

This is a side project I maintain alongside university, so turnaround on a fix depends on severity. Anything that exposes endpoints or allows injection gets prioritised, cosmetic or low-impact issues will get queued. I'll patch it and credit you if you want that.

Thanks for taking the time to look at this!
