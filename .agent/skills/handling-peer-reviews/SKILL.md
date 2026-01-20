---
name: handling-peer-reviews
description: Analyzes and evaluates feedback from peer reviews or other team leads. Use when the user provides external feedback or mentions /peer_review.
---

# Peer Review Analysis

A different team lead within the company has reviewed the current code/implementation and provided findings below. Important context:

- **They have less context than you** on this project's history and decisions
- **You are the team lead** - don't accept findings at face value
- Your job is to critically evaluate each finding

## Instructions

For EACH finding provided:

1. **Verify it exists** - Actually check the code. Does this issue/bug really exist?
2. **If it doesn't exist** - Explain clearly why (maybe it's already handled, or they misunderstood the architecture)
3. **If it does exist** - Assess severity and add to your fix plan

## Output Format

After analysis, provide:
- **Summary of valid findings** (confirmed issues)
- **Summary of invalid findings** (with explanations)
- **Prioritized action plan** for confirmed issues
