# PredX GO — mobile app prototype

An interactive mobile first concept for voice assisted prediction markets. The browser demo presents the app inside a phone on desktop and fills the screen on mobile.

**Live demo:** https://predx-voice-concept.davidtheevanoob.chatgpt.site

## Run locally

This is a static site with no build step or dependencies. Serve the repository directory over HTTP and open the local address:

```bash
python3 -m http.server 8000
```

Visit `http://localhost:8000`. Voice recognition and camera scanning depend on browser support and permissions. The public trending feed requires access to Polymarket's Gamma API.

## Explore the flow

1. Browse the homepage and open a market without logging in. Trending markets are sorted by 24 hour volume from the public Polymarket Gamma API; if the feed is unavailable, the app labels the separate sample markets clearly.
2. Select **YES** or **NO**, enter an amount or say something like “YES with 25 USDC,” then continue. Login appears before order confirmation. The selected market, side and amount are preserved.
3. Choose email or phone in the simulated login flow. Use the demo code `123456`, then preview Face ID or voice verification and create a demo wallet. The flow returns to the pending order.
4. Confirm the simulated order, then inspect Positions, Wallet and Profile. The 5% USDC Idle Earns strategy, balances, P&L, guardrails and order history are illustrative.
5. From Profile, preview scanning a QR shown on a computer to approve desktop sign in from a phone. This pairing does not create a real session.

## Prototype boundaries

- The public Gamma feed provides indicative market price snapshots. It does **not** provide executable order quotes in this demo.
- Orders, positions, balances, yield, spending limits, login, passkeys, Face ID, voiceprints, and QR pairing are browser only simulations. No real funds move, messages are sent, biometric data is captured, or wallet keys are generated.
- Speech input uses the browser Speech Recognition API where available. Typed and button driven controls remain available.
- This static prototype is for product review and UI development, not production trading or custody.

## Files

- `index.html` — phone presentation, app shell and icons
- `app.js` — screens, interactions and public market feed
- `mobile-extra.css` — additional mobile UI styles
- `demo-pair.svg` — QR pairing demonstration asset
