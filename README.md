# 🐔 ChickenLog

A backyard chicken **flock & egg log** for keepers. Log daily egg counts, track your
birds, and keep dated health / treatment records (mites, worming, vaccines, vet, notes).

**100% private and offline** — everything is stored in your own browser (localStorage).
No account, no cloud, no tracking. Works in the coop with no signal.

👉 **[Open ChickenLog](https://alexeysamosadov.github.io/chickenlog/)**

## Free, forever

- Unlimited daily egg logging with weekly / monthly / all-time totals + laying trend
- Full flock roster (name, breed, hatch/acquired date, active/lost)
- Health & treatment log — Mites/Lice, Wormer, Illness, Vaccine, Vet, Note
- Dated coop notes (predators, feed changes, maintenance)

## Pro — one-time **9 USDC**

- CSV export of egg log and health records
- Monthly egg-production charts (inline SVG)
- Multi-coop — track separate flocks independently
- Backup & restore

Licenses are issued automatically: pay USDC on Base, open an issue with the tx hash,
and a signed offline-verifiable key is posted back within ~1 minute. The key is
verified in your browser against an embedded public key — no server involved.

## How it works

Single self-contained `index.html`. License keys are ECDSA (P-256) signatures over a
small JSON payload, verified client-side via the Web Crypto API. Orders are fulfilled by
a GitHub Action (`scripts/fulfill-action.mjs`) that checks the on-chain USDC transfer and
signs a license with a private key held only as a repo secret.

Your data never leaves your device.
