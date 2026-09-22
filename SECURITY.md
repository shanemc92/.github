# Security Policy

These are personal projects. They are maintained in spare time, but security
reports are taken seriously and will get a real answer.

## Reporting a vulnerability

**Please do not open a public issue for a security problem.**

Report it privately through GitHub's private vulnerability reporting: open the
**Security** tab on the repository in question and choose **Report a
vulnerability**. That opens a private advisory visible only to you and me.

Useful things to include:

- which repository and which file or feature
- what an attacker can actually do with it
- the steps to reproduce, and a proof of concept if you have one

## Supported versions

Only the latest commit on `main` is supported. There are no maintenance
branches and no backports to tagged releases - fixes land on `main` and that
is the version to use.

| Version | Supported |
| ------- | --------- |
| latest `main` | yes |
| anything older | no |

## What to expect

Best effort, on personal-project timescales. There is no SLA. In practice:

- an acknowledgement when I see the report
- an assessment of whether it is exploitable and how bad it is
- a fix on `main` for anything that is genuinely exploitable
- credit in the advisory if you would like it

Most of these repositories are single-file, client-side HTML tools with no
server and no accounts, so the realistic issue classes are things like XSS in
a tool that renders untrusted input, a dependency pulled from a third party,
or a Content-Security-Policy that is weaker than it should be. Reports about
those are very welcome.

## Out of scope

- Findings from an automated scanner with no demonstrated impact
- Missing headers on a page that has no session and no secrets to protect
- Social engineering, physical access, or anything requiring a compromised
  machine that is already running the tool
