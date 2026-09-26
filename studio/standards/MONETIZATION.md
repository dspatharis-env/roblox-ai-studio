# Monetization Standard

## Player-first rules
- No fake scarcity.
- No false countdowns.
- No manipulative "buy now or lose everything" copy.
- Avoid interrupting the first fun moment with a purchase prompt.
- Show clear value before asking for Robux.
- Preserve a satisfying free path.

## Product types
### Pass
Use for permanent privileges/convenience/cosmetic value.

### Developer product
Use for repeatable value. ProcessReceipt is mandatory and grants must be idempotent.

### Subscription
Only when recurring monthly value exists.

### Paid random item
Avoid by default. If introduced, complete policy review, disclose actual numerical odds, handle per-user restrictions and ensure eligibility checks.

## Pricing workflow
1. Human creates product/pass.
2. Human supplies ID and initial price.
3. Code keeps ID in config.
4. Analytics tracks prompt → purchase completion.
5. Change price only with data and owner approval.
6. Consider Roblox price optimization only after enough transaction data exists.

## Prompt timing
Prefer natural value moments:
- after a round/result
- from an explicit shop action
- after player understands the benefit
Avoid:
- immediate spawn
- death frustration spam
- repeated prompts within minutes
