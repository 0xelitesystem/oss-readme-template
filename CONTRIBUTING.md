# Contributing

Thank you for considering a contribution.

## Before you start

For anything more than a typo fix, please open an issue first to discuss what you want to change. This saves both of us the time of working on something that might not get merged.

## Setup

```
git clone https://github.com/your/project.git
cd project
npm install
npm test
```

## Pull requests

- One PR per logical change. Smaller PRs get reviewed and merged faster.
- Include tests for behavior changes.
- Run `npm test` and `npm run lint` before opening the PR.
- Reference the issue number in the PR description (e.g. "Closes #42").

## Code style

We follow whatever the linter says. Run `npm run lint -- --fix` to auto-fix what's auto-fixable.

## Reporting bugs

Open an issue with:

- What you were trying to do
- What happened
- What you expected to happen
- Minimum reproduction (a code snippet or repo link)
- Your environment (OS, Node version, etc.)

## Reporting security issues

For anything security-related, please email the maintainer directly instead of opening a public issue. See [SECURITY.md](SECURITY.md) for the address.

## Code of conduct

Be kind. Disagreements about code happen; disagreements about people don't. We use the [Contributor Covenant](https://www.contributor-covenant.org/) as our standard.
