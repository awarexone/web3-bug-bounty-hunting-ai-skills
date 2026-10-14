---
name: web3-start-here
description: Master index for the web3 smart contract security knowledge base. Use this to navigate the skill chain. Read files in order — each ends with NEXT.
---

# WEB3 SKILLS — MASTER INDEX

> Built from: 2,749 Immunefi reports + 100+ paid writeups + DeFiHackLabs (681 hacks) + ConsenSys + SlowMist + Trail of Bits + Foundry + Nethermind + Lido + AI agent research + live hunt experience

---

## THE CHAIN (read in this exact order)

```
web3-start-here                 ← YOU ARE HERE
web3-hunt-foundation            ← Mindset, target selection, recon setup
web3-bug-classes                ← All 10 bug classes with patterns + real examples
web3-grep-arsenal               ← Master grep patterns for every class
web3-poc-foundry                ← Foundry PoC writing, cheatcodes, 18 exploit templates
web3-triage-report              ← 7-Question Gate, report format, 20 real paid examples
web3-methodology-research       ← ToB, SlowMist, ConsenSys, Immunefi, Cyfrin, Lido, Nethermind
web3-case-study-role-misconfig  ← Case study: role misconfiguration bug (2 findings)
web3-hunt-zksync-era            ← Completed hunt: ZKsync Era (0 findings — defense study)
web3-ai-tools                   ← Shannon, LuaN1ao, SmartGuard, CAI Framework, AI code hunting
web3-solidity-audit-mcp         ← MCP server: Slither+Aderyn+SWC in Claude Code
```

Each entry is a directory holding one `SKILL.md`.

---

## HOW TO USE THIS

1. Read one file fully — every section
2. At the bottom: follow → NEXT
3. **After `web3-triage-report`**: you can hunt independently
4. **`web3-methodology-research` through `web3-ai-tools`**: advanced tools + active work
5. **`web3-solidity-audit-mcp`**: MCP integration for live scanning

---

## QUICK STATS

| Metric | Number |
|--------|--------|
| Immunefi reports analyzed | 2,749 |
| Protocols covered | 51 |
| Critical reports | 406 |
| High reports | 616 |
| Total paid by Immunefi | $100M+ |
| Avg critical payout | $50K–$2M |
| Nethermind reports analyzed | 166 |
| DeFiHackLabs hacks reproduced | 681 |

---

## THE ONE RULE

> "Read ALL sibling functions. If `vote()` has a modifier, check `poke()`, `reset()`, `harvest()`. The missing modifier on the sibling IS the bug."

This single rule explains 19% of all Critical findings.

---

→ NEXT: [web3-hunt-foundation](../web3-hunt-foundation/SKILL.md)
