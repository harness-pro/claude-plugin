---
name: harnesspro
description: Build, test and run trading agents on HarnessPro (Solana). Use when the user wants to trade, build or change a trading agent, or check their portfolio, wallet, executions, backtests or credits on HarnessPro.
---

Everything goes through the HarnessPro MCP server (`harnesspro`). If its tools are missing or ask for a login, tell the user to run `/mcp`, pick `harnesspro` and sign in in the browser.

1. Read https://api.harnesspro.ai/llms.txt first: the app, every node and its output, the rules and the costs.
2. Ask what the user wants to trade and when.
3. Build it in paper mode, `test_run` it and show what every node did (`get_execution`). Backtest it when the past can tell something.
4. Go live only when the user explicitly asks for it: a new agent with the same graph in live mode, test it, `publish_agent` with `confirmLive: true`, then `activate_agent`. Tell them what it can spend.

Money comes in by sending USDC, USDT, PYUSD or SOL to a swarm's address (`get_wallet`). Withdrawing, raising limits, restarting a stopped swarm and buying credits only work in the web app at https://app.harnesspro.ai: say so instead of trying.
