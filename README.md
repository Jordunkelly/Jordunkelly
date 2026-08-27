# Jordan R. Kelly

Technical Lead, DoD. Pennsylvania.
[jordunkelly.github.io](https://jordunkelly.github.io)

By day I build Oracle and PL/SQL systems for the Navy. The kind that have to work the first time, for people who can't afford for them not to.

By night I build the things I wish already existed.

Eleven years in, and the part I still like best is the moment a system stops being an idea and turns into something you can actually install.

## Hoard v1.0.0, private beta

Every personal finance app wants your bank password or a Plaid token. I didn't want to hand mine over, so I built the one that doesn't ask.

Hoard reads the transaction alerts your bank already emails you and turns them into a live cash flow forecast, automatic bill detection, and spending analytics. Next.js 15 and Electron sitting on Prisma and SQLite. Your mailbox credentials get sealed against the OS keychain, so a copied database file is useless on anybody else's machine. One click installer.

1,862 unit tests across 78 files, plus 23 in the browser and 15 that run against the packaged build, because there is nobody else to catch it.

No server. No telemetry. No account. There's nothing to breach because there's nothing out there.

Buy it once, own it forever, and fixes are free. That's the deal when it ships. It isn't out yet.

## Also on the bench

**Agentic tooling.** I build through agents now, not around them. Claude Code and Antigravity, MCP servers, parallel worktrees with collision interlocks so two agents never land on the same file, and verification gates that refuse the release when a check fails. Prompt chaining and structured JSON contracts on the Claude, Grok, OpenAI, and Gemini APIs. Most of it pointed at the unglamorous half of software: release engineering, migrations, the tests nobody wants to write.

**[webworks](https://github.com/Jordunkelly/webworks).** Full stack web applications.

## How I work

I like problems where the constraint is the design. Hoard isn't allowed to phone home, and that one rule decided the storage layer, the auth model, the update channel, and the licensing. Give me a hard limit and I'll build something better inside it than I would have without it.

I read the RFC. I write the test. I ship the installer. Then I use the thing myself until something about it annoys me, and I go fix that. Repeat until it stops annoying me. Honestly, that loop is most of what I know how to do.

Day job runs on the same discipline from the other end. Three applications are mine and I'm technical lead for two developers. Agile team, work tracked in Azure DevOps Boards, and a live object Oracle deployment model where the release pipeline is mine to build and mine to answer for. Last cycle was 71,000 lines over four months. One major bug on release day, fixed in minutes. That number is the whole job.

None of it stands alone either. Data moves in and out over APIs to DAAS and DLA, so half of an integration is agreeing the contract with another agency's team and the other half is living with what you agreed.

There's no Git on that stack, which is a funny thing to write on GitHub. The rollback the platform hands you snapshots compiled object text into a table and reverts to that compile, and it is not guaranteed to come back. So the real discipline is my own object snapshots and pre staged backups on every promotion through preprod. You learn to keep the blast radius small.

I make my own art, too. The sprites, the gifs, the video, the whole 8 bit look of Hoard. That runs through the Grok API and its studio tooling instead of getting farmed out, and going from an idea to a finished asset in an afternoon quietly changes what one person is allowed to attempt.

Enterprise work taught me the discipline. Side projects are where I get to find out what I actually think.

## Tools of the trade

Build: `Oracle 19c` `PL/SQL` `Java` `TypeScript` `React` `Next.js 15` `Electron` `Prisma` `SQLite` `Tailwind` `PHP` `Vitest` `Playwright`

Ship: `Azure DevOps` `CI/CD` `Git` `Inno Setup` `code signing`

Agents and models: `Claude Code` `Antigravity` `MCP` `Claude API` `Grok API` `OpenAI API` `Gemini`

Assets: `Grok Imagine` for sprites, gifs, and video

## What I'm on right now

Taking Hoard from private beta to a public paid release. Code signing and storefront distribution.

Mail auth is staying on direct IMAP over TLS. I looked at moving to OAuth2 and decided against it: I'm not interested in holding an API key that can read a user's mailbox, and I don't think users should have to grant one to a finance app that never phones home. Where a provider still allows a direct IMAP connection the user sets up themselves, Hoard supports it. Where a provider has closed that door, I'd rather publish the compatibility list and say so plainly than pretend the door is open.
