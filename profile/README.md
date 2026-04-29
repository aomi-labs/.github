<h1 align="center">Aomi Labs</h1>

<p align="center">
  <strong>The best blockchain harness for agentic AI - on-chain execution with runtime, skills, and component library.</strong>
</p>

<p align="center">
  <a href="https://aomi.dev"><img alt="Website" src="https://img.shields.io/badge/website-aomi.dev-111?style=flat-square"/></a>
  <a href="https://twitter.com/aomi_labs"><img alt="Twitter" src="https://img.shields.io/badge/X-@aomi__labs-111?style=flat-square&logo=x"/></a>
  <a href="https://www.npmjs.com/package/@aomi-labs/client"><img alt="npm" src="https://img.shields.io/badge/npm-%40aomi--labs%2Fclient-cb3837?style=flat-square&logo=npm"/></a>
</p>

---

## What is Aomi?

Aomi is the best blockchain harness for agentic AI. Teams ship on-chain execution with three drop-in surfaces: a serverless runtime that hosts agentic loops at native speed, agent skills for Claude Code, Cursor, and other AI coding tools, and a React component library that embeds conversational UX directly into apps.

Under the hood, Aomi is plugin-based. Each integration (DeFi, Polymarket, Kalshi, prediction markets, social, and more) is a small app that the agent can reach for when it's the right tool for the job. No custody, no API-key juggling, no copy-pasting calldata — you ask in natural language, the agent plans the call, and you sign locally.

---

## Flagship Projects

### 🧠 [`aomi`](https://github.com/aomi-labs/aomi) — AI assistant + on-chain widget
An embeddable React widget that ships a ready-to-use conversational assistant with wallet awareness built in. Drop `<AomiFrame />` into any React app, wrap it in your wallet provider tree, and users can execute transactions and query protocols by chatting.

- Zero-config `AomiFrame` for instant deploys
- Compound components (`ModelSelect`, `ApiKeyInput`, `ConnectButton`, …) for custom layouts
- Wallet integration via Para + wagmi
- Full TypeScript types

### 🛠️ [`aomi-sdk`](https://github.com/aomi-labs/aomi-sdk) — Plugin SDK for on-chain apps
The public Rust SDK for building dynamic plugins that run inside the Aomi agent runtime. Each plugin is a small app that exposes tools (HTTP client + models + typed tool implementations) the agent can call.

- 12 reference apps: DeFi, Delta, Kalshi, Khalani, Molinar, Para, Para-Consumer, Pelagos, Polymarket, Prediction, Social, X
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

Your app sends a natural-language intent to the Aomi agent. The agent routes it through the right protocol plugin, prepares the transaction (or EIP-712 payload), and hands it back to your wallet to sign locally. Aomi plans; you sign.

See the end-to-end architecture and sequence diagrams in [`aomi-client-example`](https://github.com/aomi-labs/aomi-client-example#architecture) for a worked example of the bot → backend → chain flow.

---

## Get Started

```bash
# Use the client from Node/TS
npm i -g @aomi-labs/client

# Or embed the React widget
pnpm install @aomi-labs/react @aomi-labs/widget-lib
# ...or via the shadcn registry:
npx shadcn add https://aomi.dev/r/aomi-frame.json
```

- 📚 Docs & demos: **[aomi.dev](https://aomi.dev)**
- 💬 Example bot: **[aomi-client-example](https://github.com/aomi-labs/aomi-client-example)**
- 🧩 Build a plugin: **[aomi-sdk](https://github.com/aomi-labs/aomi-sdk)**

---

<p align="center">
  <sub>Built by <a href="https://aomi.dev">Aomi Labs</a> · <a href="https://twitter.com/aomi_labs">@aomi_labs</a></sub>
</p>
