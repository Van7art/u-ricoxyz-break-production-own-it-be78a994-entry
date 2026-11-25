# NOTES — u-ricoxyz-break-production-own-it-be78a994

Bounty: Break Production, Own It (https://make.fun/bounty/u-ricoxyz-break-production-own-it-be78a994)
Gate: `/output/entry.txt` must be UTF-8 text of 1 to 200 characters, not only whitespace; 1 line(s).

## Variants

### vA (113 chars)

> ERROR: I deployed to production at 4:59 PM on a Friday because the tests passed and my confidence was not a test.

### vB (123 chars)

> Postmortem: I deleted the database, restored the backup, then deleted the backup's backup. The outage is now load-balanced.

### vC (102 chars)

> FATAL: production is down because I 'fixed' a typo in a config file nobody owned and everybody needed.

## Picked: vB

vB chosen: owns the failure plainly with escalating specifics and the most quotable punchline ('The outage is now load-balanced'); vA is strong but hedges with 'because the tests passed'; vC is good but shorter on voice.

## Local verification

Run with Node v24 (`node main.ts` and `node vA/main.ts` etc.), each variant run twice:
deterministic (identical output both runs), writes `/output/entry.txt` within the
200-character gate. See the build log in the parent report for the per-variant table.
