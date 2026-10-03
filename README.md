# Telegram gold signal channel rankings

Monthly snapshots of how Telegram gold (XAUUSD) signal channels performed on real MetaTrader accounts. Every figure comes from trades that [TTMT – Telegram to MetaTrader](https://telegramtometatrader.com/?utm_source=github&utm_medium=owned&utm_campaign=gold-rankings-dataset) executed for its own users from each channel's messages. Nothing here is a backtest, a provider screenshot, or a self-reported result.

**This repository is a snapshot. The [live ranking](https://telegramtometatrader.com/explore/rankings/gold?utm_source=github&utm_medium=owned&utm_campaign=gold-rankings-dataset) is recomputed daily and is the version to cite.** A correction made on the live page reaches this repository only at the next monthly snapshot.

## October 2026

Captured 2 October 2026. 10 channels ranked across 14,662 closed trades. 47 more gold channels are listed and not yet ranked.

| # | Channel | TTMT score | Closed trades | Win rate | Profit factor | Traders in profit (90d) | Access |
|---|---|---|---|---|---|---|---|
| 1 | GiltStone Traders (FREE CHANNEL) | 4.7 / 5 | 197 | 74.1% | 3.40 | 10 of 15 | Free |
| 2 | GOLD SIGNAL USA | 4.0 / 5 | 3,493 | 55.6% | 1.38 | 12 of 24 | Free |
| 3 | Gold Trader Sunny | 3.7 / 5 | 264 | 73.5% | 1.12 | 3 of 8 | Free |
| 4 | Jonny's Trading Academy | 3.7 / 5 | 635 | 68.5% | 0.94 | 4 of 9 | Access not verified yet |
| 5 | Jonny's FX Trader | 3.3 / 5 | 1,126 | 74.5% | 1.43 | 2 of 7 | Access not verified yet |
| 6 | VIP BIG LOT | 3.3 / 5 | 1,928 | 55.9% | 0.83 | 2 of 6 | Access not verified yet |
| 7 | Jonny's Exclusive Trading School | 3.0 / 5 | 1,770 | 66.7% | 0.96 | 0 of 7 | Access not verified yet |
| 8 | GTMO VIP | 2.7 / 5 | 4,030 | 67.1% | 0.69 | 3 of 15 | Access not verified yet |
| 9 | Gold Signals 98% Sure | 2.3 / 5 | 582 | 67.3% | 0.74 | 2 of 7 | Free |
| 10 | Ben, Gold Trader | 2.3 / 5 | 637 | 58.9% | 0.51 | 1 of 9 | Free |

Two things the table shows on its own. All ten channels won more than 55% of their trades, and six of the ten have a profit factor below 1.00, meaning their losing trades cost more than their winning trades made. The channel with the highest win rate, 74.5%, ranks fifth.

## Files

| File | Rows | Contents |
|---|---|---|
| `data/2026-10-ranked.csv` | 10 | the table above, one row per ranked channel |
| `data/2026-10-listed-not-ranked.csv` | 47 | gold channels in the directory that have not reached the minimum sample, with their closed-trade count |

Columns in the ranked file:

| Column | Meaning |
|---|---|
| `rank` | position in the table |
| `channel` | channel name as shown on its TTMT page |
| `ttmt_score` | 0 to 5, the mean of the scorecard rows the channel has enough data for |
| `closed_trades` | closed executions over the channel's whole history on TTMT |
| `win_rate_pct` | trades closed in profit over all closed trades. A flat close counts in the denominator |
| `profit_factor` | gross profit divided by gross loss |
| `traders_in_profit_90d` | distinct TTMT users with net profit above zero on the channel over 90 days |
| `traders_90d` | distinct TTMT users who closed at least one trade from the channel over 90 days |
| `access` | `Free`, or `Access not verified yet` |
| `channel_page` | the channel's page on TTMT, which carries the current figures |

## How the numbers are counted

- **A trade is one execution on one MetaTrader account**, opened from a channel message and closed at the broker. Open trades are left out until they close.
- **Executions, not posts.** One message that executes on eight accounts adds eight trades. A channel with more followers accumulates trades faster.
- **Demo and live accounts are pooled.** Demo fills are kinder than live ones. Each channel page splits the two.
- **A channel is ranked once it has 100 closed trades and 5 distinct traders** in the last 90 days. Below that, one person's run decides the number.
- **Order** is TTMT score, then profit factor, then the share of traders in profit, then trade count, then alphabetical.
- **No profit or loss amount is published.** Accounts run different currencies, balances, and risk settings, so a pooled figure would describe the followers more than the channel.

The full method is on the [methodology page](https://telegramtometatrader.com/explore/methodology?utm_source=github&utm_medium=owned&utm_campaign=gold-rankings-dataset).

## What these numbers cannot tell you

Results depend on the people trading a channel as much as on the channel: their risk per trade, their broker's spread, and how they manage targets and stops. Two traders on the same signal can finish a month on opposite sides of zero. Only channels that TTMT users have connected are measured, so this is a sample of what those users follow, not a survey of Telegram. History does not expire, so a channel that changed its strategy or its owner keeps its earlier trades.

## Conflict of interest

TTMT sells the execution, not the signals. People copying channels is how the company makes money, so it has an interest in this data looking useful. TTMT takes no share of a provider's subscription revenue and is not paid for a listing or a position. Providers can join TTMT's affiliate program; that touches none of the figures here.

## Corrections

If you run a listed channel and something is wrong, message [@ttmtapp](https://t.me/ttmtapp) on Telegram or email support@telegramtometatrader.com. Names, descriptions, and access types are fixed on request. Computed figures are not adjusted on request; the disputed number is re-derived from the raw trades.

## Related

- [Signal Channels, Counted](https://telegramcopytrader.substack.com/p/gold-signal-channels-on-telegram), the monthly write-up of this data
- [We rank Telegram signal channels, and we make money when you copy them](https://medium.com/@aron.lukacs/we-rank-telegram-signal-channels-and-we-make-money-when-you-copy-them-439ea126fe5b), on the conflict of interest behind the ranking
- [telegram-signal-format](https://github.com/lukacsaron/telegram-signal-format), how the signals behind these trades are written

## Citing

> TTMT – Telegram to MetaTrader. Telegram gold signal channel rankings, October 2026 snapshot. https://telegramtometatrader.com/explore/rankings/gold

## Licence and publisher

Data and text are licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Published by jazzrabbit OÜ (registry code 16489902, Estonia).

This is not financial advice and not a recommendation to follow any channel. Past results do not predict future results. Trading leveraged products can lose you money quickly.
