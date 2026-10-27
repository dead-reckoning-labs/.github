# Security policy

This is the default security policy for every repository in the Dead Reckoning Labs organization that does not
have its own `SECURITY.md`.

## Supported versions

We support the code that is running in production today: the default branch of each repository and the version
deployed from it. Older releases, tags, forks and archived repositories do not receive security fixes. If you are
unsure whether something you found is in scope, report it anyway.

## Reporting a vulnerability

Please do not open a public issue, discussion or pull request for a security problem.

- If the repository has GitHub private vulnerability reporting turned on, use the "Report a vulnerability" button
  on its Security tab.
- Otherwise, email jamil@deadreckoninglabs.com with "Security" in the subject.

Include what you found, where (repository, URL or app), the steps to reproduce it, and the impact you think it has.
Do not include real people's personal data beyond what is needed to show the problem.

What to expect:

- We acknowledge your report within 3 business days.
- We keep you updated while we investigate and fix it, and tell you when it is resolved.
- We credit you in the fix notes if you would like, once the fix is live.

## Testing guidelines

Act in good faith: only test against accounts and data you own, do not degrade service for others (no denial of
service or load testing), do not access, change or keep other people's data, and stop and report as soon as you
find a problem. Payment and registration flows handle real money: never complete a real charge, refund or payout
while testing.
