# PredX GO — interactive prototype

A responsive PredX concept for natural language prediction markets. The desktop workspace draws on the information density and restrained trading layout of JTX, while preserving the existing mobile app flow.

**Current published mobile demo:** https://predx-voice-concept.davidtheevanoob.chatgpt.site

## Run locally

Serve the repository directory over HTTP and open `http://localhost:8000`:

```bash
python3 -m http.server 8000
```

No build step or package install is required. The desktop workspace appears at browser widths of 900px and above. Choose **Mobile preview** to inspect the phone presentation. Narrow screens show the mobile app directly.

## Desktop experience

- Browse public trending Polymarket topics ordered by 24 hour volume. YES and NO prices are indicative snapshots. If the feed cannot load, sample markets are clearly labeled.
- Search or speak a market, inspect implied probability, choose YES or NO, and enter an amount by typing, presets, or speech.
- Before confirmation, the computer shows a QR for the PredX phone app to scan. **Preview phone approval** advances this browser demo; it does not establish an actual cross-device session.
- Review the amount and guardrails, then simulate a position. Portfolio shows simulated P&L and a Close action; Wallet includes the illustrative Idle Earns strategy; Profile shows personal demo limits.

## Mobile experience

The phone app lets visitors browse markets before login. When they proceed to an order, it walks through email or phone entry, a simulated verification code (`123456`), and Face ID or voice verification. The order selection survives the login flow. The app also demonstrates wallet, positions, Idle Earns, guardrails, and phone side scanning of a computer QR.

## Prototype boundaries

The Gamma public market feed provides indicative market price snapshots, not executable quotes. Orders, positions, balances, yield, wallet creation, authentication, voiceprints, Face ID, and QR pairing are browser only simulations. No real funds move or biometric data is collected. The 5% USDC strategy is an illustrative design assumption, not a live yield or guarantee. Speech input uses the browser's Speech Recognition API where available; controls are also operable without speech.

## Files

- `index.html` — responsive shell, phone frame, and icons
- `app.js` and `mobile-extra.css` — mobile app screens and market data
- `desktop.js` and `desktop.css` — desktop trading workspace and phone approval preview
- `demo-pair.svg` — demonstration QR displayed on the computer
