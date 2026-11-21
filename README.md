# FORKAST — token site

The website for **FORKAST**, a token on Robinhood Chain.

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

```html
<iframe src="https://stoadex.com/embed/swap/robinhood/0x19D2b46b0A4D357140407D96baa207d3207Ae247?pay=ETH&ref=0x1b9cA7b297a736f4FE01256C9e2d499c79dEFFb3" width="100%" height="330" style="max-width:420px;border:0" title="Swap to FORKAST on Stoa" loading="lazy"></iframe>
```

The `ref` parameter is the referrer address for the Stoa widget bounty
entry. Swaps through the widget earn the referrer share described at
[stoadex.com/build](https://stoadex.com/build).

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
