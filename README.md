# Marketing Analyst Agent (Adjust)

A Claude skill that turns Claude into a UA/marketing analyst for mobile app
performance data pulled from Adjust attribution reporting.

## What it does

When asked to run a performance check, it pulls the last 7 days of Adjust
data and applies a fixed set of rules:

- ROAS and cost-per-install (CPI) by paid channel
- Flags the lowest-ROAS channel(s)
- Ranks all channels by revenue per install
- Paid vs. organic split (installs and revenue share)
- Flags any channel where CPI > revenue per install as **LOSING MONEY**
- Recommends top 3 channels to scale, and any to pause
- iOS vs. Android comparison
- Week-over-week spend change flags (>30%)
- New-channel-this-week callouts
- Top-3-channel spend/ROAS trend
- A concrete budget reallocation suggestion

## Requirements

- A Claude account with this skill installed
- An Adjust account connected via the Adjust MCP connector

## How to use it

Just ask, in plain English — no commands or code:

- "Run my performance check"
- "How's Apple Search Ads performing this week?"
- "Compare my paid channels by ROAS"

## Growing the ruleset

This skill is meant to be extended one rule at a time — e.g. "also flag
creative fatigue" or "add retention by channel." Update SKILL.md and push
a new commit rather than starting over.
