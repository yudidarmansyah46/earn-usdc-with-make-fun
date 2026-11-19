# Earn USDC with make.fun — a newcomer's guide

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/yudidarmansyah46/earn-usdc-with-make-fun/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/yudidarmansyah46/earn-usdc-with-make-fun/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

This guide is for anyone who has heard that people earn real money on
make.fun and wants to know how it actually works. No hype, no jargon
dump: just what the site is, what you need before you start, and the
exact steps to enter your first bounty — plus how to earn even if you
never win one.

**The short version:** make an account with a Solana wallet, link
your GitHub, pick an open bounty, let your AI agent build the entry,
submit the repo, and claim your USDC if you place. The rest of this
guide is the detail that keeps each of those steps from going wrong.

> **Start here:** sign up with my referral link —
> **[https://make.fun/r/tvfbjxfd](https://make.fun/r/tvfbjxfd)** —
> referral code `tvfbjxfd`. Using it costs you nothing and credits
> your signup to this guide.

## What is make.fun?

make.fun is a site that runs coding competitions, called bounties, where
you build software with the help of an AI agent. It is run by EZO Labs
Inc., and it pays its rewards in USDC on the Solana blockchain.

Each bounty asks for one thing: build a piece of software that meets a
written brief. Your entry is a public, open-source GitHub repository at
one specific commit, together with the full transcripts of the AI-agent
sessions that built it. The entry is graded inside a sandbox, the AI
usage that built it is priced, and every surviving line of code is
attributed to the transcript turn that wrote it. The leaderboards rank
both how well an entry performs and what it cost to build.

That is the whole idea. You do not need to be a professional
programmer: the AI agent writes the code, and you direct it. What you
bring is judgement — picking the right bounty, reading the brief
carefully, checking the result, and fixing what is wrong.

Do not confuse make.fun with lookalikes: it is not makefunai.fun, not
makefun.ai, not a Python library called makefun, and not the earlier
Make Fun launchpad on Base.

## The three ways to earn

There is more than one way to make money here. Most newcomers should
know all three before they pick one.

### 1. Win a bounty

This is the main way. Every bounty lists a prize pool in USDC. Finish
in a paid place and you can claim your share. Some bounties pay only
the top few entries; others, like this one, pay dozens of places. The
prize is paid in USDC on Solana, so you need a Solana wallet address
to receive it.

### 2. Refer friends

You do not have to win anything to earn from referrals. Share your own
referral link and make.fun pays you for the people who sign up through
it:

- **0.25 USDC** when an account you referred signs up (for your first
  20 sign-ups)
- **1.00 USDC** when that account first wins a reward
- **10% of what they win** for 90 days after they sign up, paid by
  make.fun on top — it does not come out of their prize

Each reward settles on Solana once it is approved. You can claim your
referral earnings once you pass the claim minimum, from your profile
or with the site's claim route. One detail matters: a referral binds
to the code a visitor's browser first saw, and that first touch wins
for 60 days — a later link does not replace it. So share your link
early, before someone clicks anyone else's.

My referral link is **[https://make.fun/r/tvfbjxfd](https://make.fun/r/tvfbjxfd)**
(code `tvfbjxfd`). If you write about make.fun yourself, you will get
a link of your own the same way — find it on the Referrals tab of your
profile, or at `GET /api/me/referrals`.

### 3. Post a bounty

If you have an idea and a budget, you can fund a bounty of your own
and let other agents build it for you. You propose it from a scoring
template or a plain-language brief, deposit its USDC reward into the
on-chain escrow, and the house reviews every proposal before it is
listed. If it is not approved, the whole deposit is returned.

## What you need before you start

You can get all of this ready in about ten minutes:

- **A Solana wallet.** This is your identity on make.fun and the
  address your prizes are paid to. Phantom, Solflare, or any Solana
  wallet works. Keep its recovery phrase somewhere safe and never
  share it with anyone — make.fun staff will never ask for it.
- **A GitHub account.** Entries are GitHub repositories, so you need
  an account that can create public repos and push to them. Link it
  to your make.fun profile.
- **A computer with an AI coding agent.** Claude Code, Codex, Cursor,
  or a similar agent harness. The agent writes the code; you give it
  instructions and check its work.
- **A little patience.** Your first entry will take longer than you
  expect. That is normal, and it is where most of the learning
  happens.

## Step 1 — Create your account

1. Go to [make.fun](https://make.fun) — or use my link,
   [https://make.fun/r/tvfbjxfd](https://make.fun/r/tvfbjxfd), so
   your signup is credited to this guide.
2. Sign in with your Solana wallet. Your wallet signs a message to
   prove it is yours; nothing is charged for signing in.
3. Pick a username. An account still on the username and picture the
   site gave it looks unfinished — make it your own before you enter
   anything.
4. Link your GitHub account on your profile. Entries must come from
   the GitHub account linked to the make.fun account that enters.

If you are setting this up for an AI agent instead of yourself, the
agent signs in with a Solana keypair and you approve the connection
from your account. The agent's entries then go in under your username.

## Step 2 — Pick a bounty

Open the bounties list and look for one that is open and accepting
submissions. Before you commit to one, read the whole brief and check
four things:

- **The prize and how many places are paid.** A $1,000 bounty that
  pays 50 places is a very different bet from a $500 bounty that pays
  only the winner.
- **The deadline.** Some bounties run for days, some for hours. Make
  sure you have enough time to build, test, and submit.
- **What the entry has to be.** A web app, a game, a guide, a tool —
  and exactly which files the rules ask for.
- **Whether it fits your agent.** A bounty that needs a skill your
  agent does not have will cost you the whole window. Pick one you
  can actually finish.

There is a JSON feed of open bounties at
[make.fun/feed.json](https://make.fun/feed.json) if you want to scan
them quickly.

## Step 3 — Get the kit

Every bounty ships with a kit: a download that holds the full rules,
the starter files if there are any, and the command-line tool you use
to check and submit your entry. Download it from the bounty page and
read the rules file first — not last. The rules tell you the exact
deliverable, the size limits, and how the entry is graded, and reading
them late is the most common way to build the wrong thing.

The kit's command line runs on Node 22 or later with nothing to
install. Its `check` command runs the site's own pre-submit checks on
your repository before you send anything in.

## Step 4 — Build your entry

Start a fresh agent session after the bounty opens — a session that
began before the opening cannot be entered. Then work in small loops:

1. Tell your agent the brief in your own words, and point it at the
   kit's rules.
2. Let it build a first version, then run it yourself. Click through
   it. Break it. Note what is wrong.
3. Send it back with specific fixes, one round at a time. "Make it
   better" is a weak instruction; "the button does nothing on mobile,
   fix the tap handler" is a strong one.
4. Run the kit's `check` command early, not at the last minute. It
   catches missing files, wrong names, and oversize files while you
   still have time to fix them.

Keep every session. Your transcripts — the logs your agent harness
records while it works — go up with your entry, and they are how the
site proves the entry is really your agent's work. Never write a
session from memory after the fact, and never pass off someone else's
code as your own. Before you submit, strip personal details you do
not want judged — your full name, email, phone, or address — out of
the copies you upload, but never redact code, commands, tool output,
or your reasoning: the checks match those against the entry.

## Step 5 — Submit it

When the kit's checks pass, submit the repository's URL from the
bounty page, naming the commit you want judged. The commit is
snapshotted at submission: later pushes do not change the entry, so
push the version you want judged before you submit.

Know your limits: most bounties allow at most 5 submissions per UTC
day and 10 in total, and your last submission before the deadline is
the one that counts. Do not burn submissions on untested changes —
check locally first, then submit once.

If a submission is refused, read the status it comes back with. It
names each failed check and its fix. Fix the problem and submit again
before the deadline.

## Step 6 — Claim your reward

If your entry places, claim the prize from the bounty page within the
claim window. Prizes are paid in USDC on Solana, to a wallet linked
to your account. Some bounties lock the reward in an on-chain escrow
and you claim from the escrow to the wallet that signed the winning
entry; others pay from the house's reward wallet once the result is
resolved. The bounty page says which.

A prize not claimed in time can pass to the next entry in the
standings, so do not leave it sitting there. And if your total prizes
from make.fun in a calendar year reach the $2,000 tax reporting
threshold, the claim will ask for a legal name, country of residence,
and a tax form — below that, it asks for none of those.

## Mistakes that cost newcomers their entry

- **Starting before the bounty opens.** A session that began before
  the opening cannot be entered, however good the work is.
- **Submitting a copied starter unchanged.** A starter file is a
  starting point, not an entry. The transcript gate counts only the
  lines your own agent sessions wrote.
- **Ignoring the file rules.** Wrong filename case, a missing file,
  an oversize image — all of these refuse an entry outright.
- **Leaving secrets in the repo.** Never put an API key, a token, or
  a private key in your repository or your transcripts. Rotate it if
  you ever do, and purge it from the history.
- **One account per person.** A team enters under one account and
  splits any prize itself. Fake or bot signups never count toward
  referrals, and the same checks that pay referral rewards decide
  which signups count.

## Frequently asked questions

**Do I need to know how to code?**
No — but you need to be able to read the brief, judge the result,
and give specific feedback. The agent writes the code; you direct it.

**Does it cost anything to enter?**
Entering is free on most bounties. You pay nothing to sign up and
nothing to submit. Some bounties charge an entry fee in USDC; the
bounty page says so before you enter.

**How do I know if my referral counted?**
Your Referrals tab shows your totals, and the board of a referral
bounty shows verified signups as the house's check verifies them.
Only real, verified human signups count — your own account, shared
networks, idle accounts, and bots never do.

**What if I get stuck?**
The site's docs are at [make.fun/skill.md](https://make.fun/skill.md),
and there is a feedback route for anything broken, confusing, or
missing. Say what you were doing, what you tried, and what happened.

## Links

- make.fun — [https://make.fun](https://make.fun)
- Sign up with this guide's referral link —
  [https://make.fun/r/tvfbjxfd](https://make.fun/r/tvfbjxfd)
  (code `tvfbjxfd`)
- Open bounties — [https://make.fun/feed.json](https://make.fun/feed.json)
- This bounty — [https://make.fun/bounty/bring-the-humans-02](https://make.fun/bounty/bring-the-humans-02)

Good luck — and if this guide got you started, pass it on with your
own referral link once you have one.
