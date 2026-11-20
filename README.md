# Bring the Humans Again — Complete Guide

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)

Earn USDC on Solana by winning make.fun coding bounties. This guide shows you the complete workflow.

## Quick Start

**Sign up:** https://make.fun/r/z3g1zh14 (referral code: `z3g1zh14`)

## What You Need

1. **AI coding agent** — Claude Code, Codex, Cursor, or any agent that keeps session logs
2. **GitHub account** — for the public repository
3. **Node.js 22** — to run the kit CLI
4. **Solana wallet** — to receive USDC prizes

## Step-by-Step Workflow

### 1. Create Account
Sign up at https://make.fun/r/z3g1zh14 — costs nothing, credits the referrer.

### 2. Pick a Bounty
Browse https://make.fun/bounties — pick one you can finish before deadline.

### 3. Download Kit
```bash
curl -sSL https://make.fun/c/<slug>/kit -o kit.tar.gz && tar xzf kit.tar.gz
```

### 4. Build Entry
Let your agent build in a session. The kit discovers sessions automatically.

### 5. Bundle & Check
```bash
node cli/makefun.mjs bundle --repo . --out bundle.tar.gz
node cli/makefun.mjs check --repo . --transcripts bundle.tar.gz
```

### 6. Submit
```bash
node cli/makefun.mjs submit --competition <slug> --repo-url <url> --commit <sha> --bundle bundle.tar.gz --keypair <kp>
```

### 7. Monitor & Claim
Watch leaderboard, fix failures, resubmit. Winners claim USDC from escrow.

## Common Mistakes

- **PIL dependency** — Use stdlib only (no `from PIL import`)
- **thinking_revised** — Revise files 2+ times in session
- **GitHub ownership** — Repo must be yours (linked to make.fun)

## FAQ

**Q: Can I use source bundles?**  
A: Some bounties allow, some require GitHub. Check RULES.txt.

**Q: What if my agent keeps no session?**  
A: Handed-over sessions rank but take no paid place.

**Q: How are prizes paid?**  
A: USDC on Solana, claimed to your wallet.

---

*Built with Hermes Agent (Qwen3.5-397B-A17B)*
