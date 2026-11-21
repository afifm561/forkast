# FORKAST — prediction market for crypto and esports

The website for **FORKAST**, a prediction market for crypto and esports
on Robinhood Chain.

- Contract: [`0x19D2b46b0A4D357140407D96baa207d3207Ae247`](https://robinhoodchain.blockscout.com/token/0x19D2b46b0A4D357140407D96baa207d3207Ae247)
- Chain: Robinhood Chain (chain ID 4663)
- Total supply: 1,000,000,000 FORKAST, 18 decimals

## What this site is

A single static page (`index.html`, no build step, no external
dependencies) with:

- the Stoa swap widget for FORKAST (buy with ETH or USDG),
- the token details and contract address,
- links to Blockscout, GeckoTerminal and the Pons launchpad.

## The widget

The Stoa swap widget is added to this page by the site owner (Apip).
The snippet to paste inside the `.widget-box` section of `index.html`,
replacing the placeholder button:

```html
<iframe src="https://stoadex.com/embed/swap/robinhood/0x19D2b46b0A4D357140407D96baa207d3207Ae247?pay=ETH&ref=0x1b9cA7b297a736f4FE01256C9e2d499c79dEFFb3" width="100%" height="330" style="max-width:420px;border:0" title="Swap to FORKAST on Stoa" loading="lazy"></iframe>
```

The `ref` parameter is the referrer address for the Stoa widget bounty
entry. Swaps through the widget earn the referrer share described at
[stoadex.com/build](https://stoadex.com/build). The snippet above was
verified live on 22 Nov 2026: it renders "Buy FORKAST" and Stoa quotes
ETH → FORKAST with ~0.07% price impact on 0.001 ETH.

## Run it locally

Open `index.html` in a browser, or serve the folder:

```sh
python3 -m http.server 8000
```

## Deploy

This repo is published with GitHub Pages (Settings → Pages → Deploy from
the `main` branch, `/` root).

## License

MIT — see `LICENSE` if present; otherwise the code in this repo is
released under the MIT license.
