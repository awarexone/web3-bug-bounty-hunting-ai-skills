<div align="center">

# web3-bug-bounty-hunting-ai-skills

Smart contract bug bounty skills for Claude Code, Claude AI, and other AI tools.
Built from 2,749 Immunefi reports, 681 DeFiHack reproductions, and real hunts.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)
[![Skills](https://img.shields.io/badge/skills-11-blue)]()
[![Immunefi](https://img.shields.io/badge/Immunefi%20reports-2%2C749-orange)]()
[![DeFiHackLabs](https://img.shields.io/badge/DeFiHack%20reproductions-681-red)]()

Built and maintained by **AwareXone** - [Website](https://awarexone.com) · [X](https://x.com/awarexone) · [GitHub](https://github.com/Awarexone)

</div>

---

Most hunters still do everything manually. Read contracts in a browser, grep from memory, rewrite Foundry templates each hunt, draft reports from scratch.

These skill files load into Claude Code (or any AI) and give it a complete smart contract security knowledge base - target scoring, bug patterns, grep arsenal, PoC templates, report format, and real case studies. One `claude` command, then start hunting.

Works with: **Claude Code**, **Claude.ai**, **Cursor**, **any AI that reads files**.

---

## Files

Each skill is a directory with one `SKILL.md`.

| Skill | Contents |
|------|----------|
| [`web3-start-here`](./web3-start-here/SKILL.md) | Index + how to navigate |
| [`web3-hunt-foundation`](./web3-hunt-foundation/SKILL.md) | Hunter mindset, target scoring (10-point scorecard), recon setup |
| [`web3-bug-classes`](./web3-bug-classes/SKILL.md) | All 10 bug classes - patterns, Solidity examples, real Immunefi findings |
| [`web3-grep-arsenal`](./web3-grep-arsenal/SKILL.md) | Grep/regex patterns for every bug class |
| [`web3-poc-foundry`](./web3-poc-foundry/SKILL.md) | 18 Foundry PoC templates - fill in address, run `forge test` |
| [`web3-triage-report`](./web3-triage-report/SKILL.md) | 7-question validation gate, Immunefi report format, 20 paid examples |
| [`web3-methodology-research`](./web3-methodology-research/SKILL.md) | Trail of Bits, SlowMist, ConsenSys, Cyfrin, Nethermind methodology |
| [`web3-case-study-role-misconfig`](./web3-case-study-role-misconfig/SKILL.md) | Full hunt walkthrough - role misconfiguration bug, real findings |
| [`web3-ai-tools`](./web3-ai-tools/SKILL.md) | Shannon, SmartGuard, CAI Framework, LuaN1ao agent setup |
| [`web3-hunt-zksync-era`](./web3-hunt-zksync-era/SKILL.md) | Defense study - 25 attack vectors tested on a hardened L2 bridge |
| [`web3-solidity-audit-mcp`](./web3-solidity-audit-mcp/SKILL.md) | MCP server - run Slither + Aderyn + SWC inside Claude Code |

Read in order. Each skill ends with `→ NEXT`. After `web3-triage-report` you can hunt on your own.

---

## The 10 Bug Classes

```
01  Accounting Desync    →  most common Critical (37% of all payouts)
02  Access Control       →  most common High
03  Incomplete Path      →  missing modifier on a sibling function
04  Off-by-One           →  boundary operators, index errors
05  Oracle Price         →  TWAP manipulation, stale prices
06  ERC4626 Vaults       →  share inflation, rounding attacks
07  Reentrancy           →  cross-function, cross-contract, read-only
08  Flash Loan           →  price manipulation, economic attacks
09  Signature Replay     →  cross-chain replay, missing nonce/chainId
10  Proxy/Upgrade        →  uninitialized implementation, storage collision
```

> Read ALL sibling functions. If `vote()` has a modifier, check `poke()`, `reset()`, `harvest()`.
> The missing modifier on the sibling is the bug. This one rule explains 19% of all Criticals.

---

## Setup

**Option 1 - drop into your existing project:**

Claude Code finds a skill only at `.claude/skills/<skill-name>/SKILL.md`, one level deep. Cloning the
repo into `.claude/skills/web3` nests every skill one level too deep, so none of them load. Copy the
skill directories up instead:

```bash
git clone https://github.com/Awarexone/web3-bug-bounty-hunting-ai-skills.git /tmp/web3-skills
mkdir -p .claude/skills
cp -r /tmp/web3-skills/web3-* .claude/skills/
claude
```

Use `~/.claude/skills/` instead of `.claude/skills/` to make them available in every project.

Then in Claude Code:
```
Start with the web3-start-here skill
```

**Option 2 - standalone workspace:**

```bash
git clone https://github.com/Awarexone/web3-bug-bounty-hunting-ai-skills.git
cd web3-bug-bounty-hunting-ai-skills
claude
```

**Option 3 - just the essentials:**
```
Read web3-bug-classes/SKILL.md and web3-poc-foundry/SKILL.md
```

---

## Numbers

| | |
|---|---|
| Immunefi reports analyzed | 2,749 |
| Critical findings | 406 |
| High findings | 616 |
| Total paid by Immunefi | $100M+ |
| DeFiHackLabs reproductions | 681 |
| Nethermind audit reports | 166 |
| Protocols covered | 51 |

---

## Related

| Repo | What it does |
|------|-------------|
| [Agentic-Bug-Hunter](https://github.com/Awarexone/Agentic-Bug-Hunter) | Point at a target → full attack surface map + Immunefi/Bugcrowd report |
| [public-skills-builder](https://github.com/Awarexone/public-skills-builder) | Feed 500 public writeups → get skill files like these back out |

---

MIT License. Use it, fork it, build on it.
