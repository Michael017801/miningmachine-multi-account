# OreFarm Console

[简体中文](README.md) ｜ **English**

A multi-account mining client for [miningmachine.io](https://miningmachine.io/).

## What it is

Mining on miningmachine.io works like a daily check-in: each account starts once per day and produces `$ORE` automatically for the next 24 hours. Managing several accounts by hand means logging in and clicking through each one every day, and a single missed day breaks the streak.

This client automates the whole routine: bulk account creation, bulk start, automatic renewal on expiry, and isolated X identity management — all from one window.

## Features

- **Bulk creation** — up to 50 accounts at once, 4 parallel logins, about 25 seconds for 50
- **Auto-renewal** — watches each session's expiry and starts the next 24-hour round automatically
- **Session isolation** — every account keeps its own token and its own X login state
- **X identity binding** — built-in authorization window, each account can bind its own X identity
- **One-click export** — export a single account or the whole list
- **Bilingual UI** — switch between Chinese and English, the choice is remembered
- **Live log** — every action and error streams into the side panel

## Interface

```
┌──────────────────────────────────────────────────────────────┐
│  OreFarm Console    Accts 12  Mining 8  Total 4.21   0.01305  │
├──────────────────────────────────┬───────────────────────────┤
│  Account       Session  Bal  MP  │  Activity                 │
│  ─────────────────────────────── │  ───────────────────────  │
│  SpicyMouse   Mining  0.32  180  │  [23:01:12] Session start │
│  KiloAxolotl  Mining  0.28  180  │  [23:01:14] Reward claimed│
│  YieldOctopus Idle    0.00   10  │  [23:04:33] Expired →     │
│  ...                             │              auto-renewed │
├──────────────────────────────────┴───────────────────────────┤
│  ● Scheduler running  Disable  Sync once      next check 12s  │
└──────────────────────────────────────────────────────────────┘
```

## Download

Grab the latest installer from [Releases](../../releases) and run it.

## How to use

1. **Create accounts** — click “+ New”, enter a count, wait for it to finish
2. **Link X** — click “Link X” on a row and authorize in the popup window
3. **Start mining** — click “Start” to open that account's 24-hour session
4. **Enable auto-renew** — click “Enable auto-renew” at the bottom and leave it running
5. **Check back** — the UI resyncs every 30 seconds, balance and remaining time update live

## Note

Each account needs its own X identity, and one X identity can only be bound to a single account. How many accounts you can run is limited by how many X accounts you have.

## Disclaimer

This project is for learning and technical research only. Automated tooling may violate the target site's terms of service; any consequences are the user's own responsibility. Follow the platform's rules.
