<h1 align="center">Aomi Labs</h1>

<p align="center">
  <strong>The on-chain AI transaction builder.</strong><br/>
  Chat your way through DeFi — swaps, transfers, prices, and strategies, signed from your own wallet.
</p>

<p align="center">
  <a href="https://aomi.dev"><img alt="Website" src="https://img.shields.io/badge/website-aomi.dev-111?style=flat-square"/></a>
  <a href="https://twitter.com/aomi_labs"><img alt="Twitter" src="https://img.shields.io/badge/X-@aomi__labs-111?style=flat-square&logo=x"/></a>
  <a href="https://www.npmjs.com/package/@aomi-labs/client"><img alt="npm" src="https://img.shields.io/badge/npm-%40aomi--labs%2Fclient-cb3837?style=flat-square&logo=npm"/></a>
</p>

---

## What is Aomi?

Aomi turns natural language into on-chain actions. Ask for a price, a swap, a transfer, or a full portfolio strategy — the agent plans the call, prepares the transaction, and hands it back to **your** wallet to sign. No custody, no API-key juggling, no copy-pasting calldata.

Under the hood, Aomi is a plugin-based runtime: each protocol (CoW Swap, Polymarket, Kalshi, prediction markets, social, and more) is a small app that the agent can reach for when it's the right tool for the job.

---

## Flagship Projects

### 🧠 [`aomi`](https://github.com/aomi-labs/aomi) — AI assistant + on-chain widget
An embeddable React widget that ships a ready-to-use conversational assistant with wallet awareness built in. Drop `<AomiFrame />` into any React app, wrap it in your wallet provider tree, and users can execute transactions and query protocols by chatting.

- Zero-config `AomiFrame` for instant deploys
- Compound components (`ModelSelect`, `ApiKeyInput`, `ConnectButton`, …) for custom layouts
- Wallet integration via Para + wagmi
- Full TypeScript types

### 🛠️ [`aomi-sdk`](https://github.com/aomi-labs/aomi-sdk) — Plugin SDK for on-chain apps
The public Rust SDK for building dynamic plugins that run inside the Aomi agent runtime. Each plugin is a small, sandboxed app that exposes tools (HTTP models + typed tool implementations) the agent can call.

- 12+ reference apps: CoW Swap, Polymarket, Kalshi, Khalani, Para, Pelagos, Molinar, Delta, DeFi, Social, X, Prediction
- `xtask` build toolchain: `cargo run -p xtask -- build-aomi`
- Documented host interop contracts
- Clear split between public SDK and private runtime

### 🎯 [`skills`](https://github.com/aomi-labs/skills) — Agent skills for your coding assistant
Drop-in skills that teach Claude Code, Cursor, Gemini CLI, and VS Code Copilot how to use Aomi.

- **`aomi-build`** — build Aomi apps and plugins with awareness of the runtime, SDK, and product specs
- **`aomi-transact`** — construct and execute EVM transactions conversationally via the `aomi` CLI

### 📈 [`aomi-client-example`](https://github.com/aomi-labs/aomi-client-example) — Build a trading bot in a weekend
A momentum-following portfolio bot built with `@aomi-labs/client`. Shows how to run your own strategy logic locally while delegating execution to Aomi — including EIP-712 signing, auto-signing with `viem`, and plain-English trade instructions.

---

## How It Works

```
   ┌──────────────┐      natural language       ┌──────────────┐
   │  Your app /  │ ─────────────────────────▶  │  Aomi Agent  │
   │  chat / bot  │ ◀── tx payload to sign ──── │  + plugins   │
   └──────────────┘                             └──────┬───────┘
          │                                            │
          │ signs with your wallet (viem / Para)       │ calls protocol apps
          ▼                                            ▼
   ┌──────────────┐                             ┌──────────────┐
   │  EVM chains  │ ◀────  broadcast tx ───────│ CoW · Polymkt│
   │              │                            │ Kalshi · ... │
   └──────────────┘                             └──────────────┘
```

**Your keys stay with you.** Aomi plans and prepares — you sign and send.

---

## Get Started

```bash
# Install the client
npm i -g @aomi-labs/client

# Or embed the widget
npm i @aomi-labs/aomi
```

- 📚 Docs & demos: **[aomi.dev](https://aomi.dev)**
- 💬 Example bot: **[aomi-client-example](https://github.com/aomi-labs/aomi-client-example)**
- 🧩 Build a plugin: **[aomi-sdk](https://github.com/aomi-labs/aomi-sdk)**

---

<p align="center">
  <sub>Built by <a href="https://aomi.dev">Aomi Labs</a> · <a href="https://twitter.com/aomi_labs">@aomi_labs</a></sub>
</p>
