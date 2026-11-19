# Gazdura

An independent AI guide to airline loyalty, built inside the AI assistant people already use. It starts with Alaska Atmos Rewards and is in early, founder-led testing.

**My role:** I designed and built Gazdura from zero to one without a human team. I set the product direction, the quality bar and the release approval rules, and led the build with AI agents.

[Project website](https://gazdura.com)

## Problem

I used to shop for flights mainly by price and convenience. Learning how status, points, perks and alliances fit together changed how I thought about a trip: not just today's fare, but what a choice could mean for future travel.

The rules are scattered and conditional. Fare, timing, eligibility and who is traveling can all change the answer. Official pages sometimes disagree, and the rules change. I wanted to make them easier to understand without expecting every traveler to become a program expert, and without an assistant guessing where the rules are unclear.

## Product

- **Advice inside an existing assistant.** A connector gives Claude or ChatGPT reviewed program knowledge, so travelers do not need to learn another travel app.
- **Understanding before transactions.** Gazdura explains rules. It does not book travel or access a traveler's airline account, balance or live seats.
- **No airline credentials.** The guest connector needs neither a Gazdura account nor an airline login.
- **A deliberately narrow starting point.** Alaska Atmos Rewards first, with partial coverage of earning, checked bags, upgrades, companion fares, airline credit cards and status on alliance partners. Companion fares and credit cards have thinner coverage.

## Architecture

- **An MCP connector serving a versioned, reviewed set of rules.** Program rules are written up as individual entries from the airline's and alliance's published pages. Each entry keeps its source, the date it was checked and the conditions that apply.
- **A versioned publication.** The connector serves one reviewed publication at a time. Changes ship as a new version, so what the assistant receives matches a known, reviewed version.
- **The assistant asks for focused sections.** The assistant handles the conversation and any math. The connector returns complete entries for the sections it asks for, with their conditions and citations.
- **Conditions are never cut.** If an entry would not fit in a response, the publication is blocked rather than shortened. A rule without its conditions is a wrong answer.

## How it handles the hard parts

- **Changing rules.** Reviewed rules carry a checked date. Depending on the rule, Gazdura flags an overdue review or withholds the entry.
- **Conflicts and gaps.** Gazdura flags unresolved conflicts and coverage gaps rather than guessing, for example on some partner earning details.
- **Questions it cannot answer reliably.** Lounge access is one example: paid Alaska Lounge membership rules do not settle whether a traveler's Atmos status gets them into an Alaska Lounge on a particular trip. Gazdura flags that gap and treats oneworld status as a separate question. How the assistant explains those limits is part of what I test.

## Evidence

Each item below says what kind of evidence it is.

- **Internal pre-release test.** An adversarial test I directed exposed incomplete rule entries. The revised build rejects them, and a regression test verified the fix. This was not a production incident.
- **Founder-led testing.** Early chats exposed an incorrect answer, and also an assistant that did not use the connector at all. That made the whole experience the test: not only whether the reference material is correct, but whether the assistant uses it and communicates its limits.
- **Live service.** The connector is live. New-user onboarding and broader rollout have not yet been verified.
- **Not yet shown.** There is no adoption, customer or conversion evidence yet. Testing so far is not broad customer validation.

## Decisions

- **Build into assistants people already use** instead of a standalone app, to remove the need to learn another tool.
- **No accounts and no airline logins** for the guest connector, to keep setup light and avoid holding travelers' credentials.
- **Block a publication rather than truncate a rule,** because a rule served without its conditions is worse than no answer.
- **Keep conflicts and gaps visible** instead of resolving them by guesswork.
- **Start narrow with one program,** and treat other airlines and assistants as directions to earn, not current coverage.

## Where it could go

My working hypothesis is that clearer loyalty guidance can help travelers judge the longer-term value of an airline ecosystem, not only the cheapest fare. That is a hypothesis to test, not a demonstrated conversion or retention result.

I see this work as a way to show what an advisory layer could offer travelers and the businesses that serve them.

---

Gazdura is independent and not affiliated with or endorsed by any airline or loyalty program. Coverage is partial and rules change. Confirm with the airline before booking.
