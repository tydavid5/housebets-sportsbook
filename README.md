# Housebets Sportsbook

Most sportsbooks only pay you when you win. When you lose, your money is just gone.

Housebets is the sportsbook where losing still pays. Every bet is on-chain and provably fair. Every loss returns up to 2% in USDT the instant it settles, with a visible on-chain receipt. Your Daily Dividend grows with every bet you place, and your membership tier climbs with it. Three clicks to your first bet. Paid the second you win.

## What this is

A clickable sportsbook prototype for the Housebets Contest Labs Design contest ($15,000). One static file, no build step, no backend. Open `index.html` in a browser, or serve the folder with any static host.

## The five pages

1. **Sports home**: search built in, top leagues, live fixtures with ticking scores and odds, upcoming today and tomorrow.
2. **Live**: every match in play right now, with the minute, the score and odds that move as the game moves, plus any suspended matches.
3. **Football**: every football league, each with its league table and fixtures, live scores and dates.
4. **Match page**: team form and stats, live odds and all markets (match result, total goals, both teams to score, double chance, draw no bet). Tap odds to add a single to your slip.
5. **Bet slip and My bets**: singles only. Enter a stake, see the potential return, place the bet. Placed bets show as open, then settle as won, lost or void.

## Every state: suspended, changed, failed

A sportsbook that only shows the happy path is not one you would ship tomorrow.

- **Suspended**: Arsenal vs Real Madrid sits suspended on the Live page from the first load (VAR check), with greyed-out odds and a banner on its match page. Arsenal vs Chelsea also suspends live about 15 seconds after the page loads, then resumes, so the state appears during normal play.
- **Changed**: add a live selection to the slip and wait a few seconds. When the odds drift, the slip shows an "Odds changed" notice with the old and new odds, and Accept new odds or Remove. The bet cannot be placed until the change is accepted or the bet is removed.
- **Failed**: place a bet while its market is suspended and it fails with a clear error and a Retry button. The failed bet never becomes an open bet, and retrying works once the market reopens.

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
