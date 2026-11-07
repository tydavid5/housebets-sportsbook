# Housebets Sportsbook

Most sportsbooks only pay you when you win. When you lose, your money is just gone.

Housebets is the sportsbook where losing still pays. Every bet is on-chain and provably fair. Every loss returns up to 2% in USDT the instant it settles, with a visible on-chain receipt. Your Daily Dividend grows with every bet you place, and your membership tier climbs with it. Three clicks to your first bet. Paid the second you win.

## What this is

A clickable sportsbook prototype for the Housebets Contest Labs Design contest ($15,000). One static file, no build step, no backend. Open `index.html` in a browser, or serve the folder with any static host.

## The five pages

1. **Sports home**: search, top leagues, live fixtures with ticking scores and odds, upcoming today and tomorrow.
2. **Search**: live filtering over teams and leagues, fixtures for today and tomorrow, tap any fixture to open its match page.
3. **League**: every fixture in that league, live scores and dates, tap any fixture to open its match page.
4. **Match**: team form and stats, live odds and all markets (match result, total goals, both teams to score, double chance, draw no bet). Tap odds to add a single to your slip.
5. **Bet slip and My bets**: singles only. Enter a stake, see the potential return, place the bet. Placed bets show as open, then settle as won, lost or void.

## The god-tier ability: Loss-back, live

The instant a bet settles as a loss, 2% of the stake lands in the balance in USDT, with a sample on-chain receipt shown on the bet. No claim step, no waiting. Wins pay out instantly too. A live Daily Dividend meter and membership tier (Bronze to Silver, Gold, Diamond) sit in the header and grow with every bet.

## Sample data only

All fixtures, odds, scores, balances, dividends and receipts are samples made for this prototype. No real money, no real bets, no real player data, no odds from other sportsbooks.

## Files

- `index.html`: the whole prototype, HTML, CSS and JavaScript in one file.
- `big-idea.txt`: the concept, 319 characters.
- `tools.txt`: the tools used, honestly named.

## Run it

```sh
python3 -m http.server 8000
```

Then open http://localhost:8000/index.html
