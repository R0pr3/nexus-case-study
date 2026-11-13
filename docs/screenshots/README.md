# Screenshots

Sanitized screenshots of the platform belong in this directory. The production
system is private, so every image must be reviewed before publication.

## Sanitization checklist

Before committing an image, confirm it contains **none** of the following:

- [ ] Customer or employee names, e-mails, phone numbers
- [ ] Internal domains, subdomains or hostnames
- [ ] Real public or private IP addresses (replace with documentation ranges:
      `192.0.2.0/24`, `198.51.100.0/24`, `203.0.113.0/24`)
- [ ] Device serial numbers, IMEIs or contract identifiers
- [ ] Tokens, cookies, bearer headers or API keys
- [ ] Browser tabs, bookmarks, OS notifications or clock details that leak context
- [ ] Map locations or site addresses

## Recommended set

| File | Shows | Notes |
|---|---|---|
| `dashboard-overview.png` | Operational dashboard | Blur all names and totals |
| `job-workflow.png` | Job dispatch to completion | Use fictional job ids |
| `device-diagnostics.png` | SSH diagnostic output panel | Fake hostnames only |
| `perimeter-dashboard.png` | UFW / Fail2Ban / container health | Run on a lab host |
| `architecture-overview.png` | Rendered Mermaid topology | Generated from `docs/architecture/*.mmd` |

## Process

1. Capture on a lab environment or a demo dataset — never on production data.
2. Redact with a rectangle fill (not blur) over sensitive regions.
3. Re-read the checklist above.
4. Commit with a descriptive message, e.g. `docs: add sanitized job workflow screenshot`.

If a screenshot cannot be sanitized with confidence, do not publish it.
