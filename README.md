# Complexe Claude-Robillard Gym QR Guide (unofficial demo)

**QR machine-instruction app skinned for a Complexe Claude-Robillard club demo.** Members scan a QR on a machine → bilingual (EN/FR) how-to guide. Staff manage machines, download QRs, print floor sheets, and review ROI insights.

> **Unofficial demo mockup for pitching only.** Not affiliated with Complexe Claude-Robillard or any parent company. Does **not** use official logo image assets — text wordmark only. Brand colors (`#00853F` / `#102418`) are approximate pitch tokens.

Seeded demo gym: **Complexe sportif Claude-Robillard**. `/` is the **demo-ready member product UI** — not a marketing landing page.

Sibling (generic GymQR Guide): [gym-machine-qr-guide](https://github.com/alexbalut/gym-machine-qr-guide)

## Disclaimer

This repository is an **unofficial product demo**. Complexe Claude-Robillard® and related marks belong to their respective owners. Do not represent this app as an official Complexe Claude-Robillard product. No official logos are bundled.

## Quick start

```bash
cd complexe-claude-robillard-gym-qr-guide
cp .env.example .env
npm install
npx prisma db push
npm run seed
npm run dev
```

Or one-shot setup:

```bash
npm install && npm run setup && npm run dev
```

Open [http://localhost:3000](http://localhost:3000) — member gym home for **Complexe sportif Claude-Robillard** (Machines / Workout / Progress / Scan).

## Demo credentials

| Field    | Value                    |
|----------|--------------------------|
| Email    | `admin@complexe-claude-robillard.demo`        |
| Password | `demo1234`             |
| Gym      | Complexe sportif Claude-Robillard                |
| Slug     | `complexe-claude-robillard`           |

Seed creates **10 bilingual machines**, sample view counts, and a few open/resolved issues.

## Branding notes

- Surfaces use secondary `#102418` with primary accent **`#00853F`**
- Text wordmark **Complexe Claude-Robillard** — no trademarked logo files
- Tagline: “Ville de Montréal”

## Key routes

| Route | Description |
|-------|-------------|
| `/` | Gym member home |
| `/scan` | Camera QR scan |
| `/q/[token]` | Machine guide |
| `/m/complexe-claude-robillard/[machineSlug]` | Friendly slug URL |
| `/admin/login` | Staff login |
| `/admin/insights` | Owner ROI dashboard |

## Caveats

- Auth is simple credential + JWT cookie — fine for demo; harden for production.
- SQLite at `prisma/dev.db` — don’t commit it.
- Member workout/progress is browser localStorage only (`complexe-claude-robillard-workout:v1:<slug>`).
- Unofficial branding — do not ship as an official Complexe Claude-Robillard app.

## Photo credits

Demo photos under `public/machines/` are from Unsplash — see [CREDITS.md](./CREDITS.md). Not official Complexe Claude-Robillard assets.

## License / affiliation

This repository is an **unofficial product demo mockup** for pitch purposes. Complexe Claude-Robillard® and related marks belong to their respective owners. Do not represent this app as an official Complexe Claude-Robillard product.

## Repo

https://github.com/alexbalut/complexe-claude-robillard-gym-qr-guide
