---
layout: post
title: 'Wealth dashboard: a Claude skill that builds a private view of your net worth'
date: 2026-11-08 21:19:13 +0000
project_link: https://dancingpea.github.io/wealth-dashboard/
---

I built a Claude skill that interviews you about what you and your household own and owe, then builds a private dashboard of your finances. A short monthly check-in keeps it current. There is no app, no server and no spreadsheet to maintain, and it works on every Claude plan. It is for people who want a clear picture of their net worth, cash, spending, goals and investments, alone or as a household.

The demo uses an invented household. Every person and number in it is made up.

## Why I built it

Claude Code makes it cheap to build software for your own use, so the tool can fit how you think about money instead of the other way round. I wanted a good sense of where I stand, not a perfect ledger, and I wanted setup to be something you can pass on as a link.

## How it works

Say "Set up my wealth dashboard" and Claude asks plain questions for about 15 minutes. Rough numbers are fine. You can answer with screenshots or exports, and an existing spreadsheet can be imported for history. No passwords, PINs or account numbers are asked for or stored.

The dashboard has four tabs:

- **Overview:** net worth, assets and debt, per person and for the household, wealth over time, and how you compare with other households in the countries you pick.
- **Cash & spending:** cash in months of spending, income against spending, and where the money goes.
- **Goals:** the 50/30/20 rule, and custom goals with deadlines, plus the date each one is reached at your current pace. A 30-year projection is included.
- **Investments:** every position with its gain since purchase, by asset class and account, with a price chart per position.

A monthly check-in refreshes prices, exchange rates and balances, then asks for the two or three numbers it still needs. You change things by asking in plain language, such as "add a goal of 500k by 2032".

Connectors are optional and read-only, and most banks don't have one, so screenshots or exports are the usual route.

## Install

In the Claude app, download the zip from the repo, turn on Code execution and file creation in Settings > Capabilities, upload it under Customize > Skills, then say "Set up my wealth dashboard."

In Claude Code:

```
/plugin marketplace add dancingpea/wealth-dashboard
/plugin install wealth-dashboard@wealth-dashboard
```

The code is MIT licensed and the repo is public. Dashboard labels are in English for now, although Claude talks with you in your language. Values are estimates, not financial, tax or investment advice.

Live demo: https://dancingpea.github.io/wealth-dashboard/
