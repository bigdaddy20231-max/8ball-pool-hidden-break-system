# 8 Ball Pool Hidden Break System

## Hidden Break Credit Theory (HBCT)

A community-derived hypothesis about how **8 Ball Pool** may assign the opening break.

> This is NOT leaked Miniclip code and is NOT officially confirmed.
> It is a mathematical model inferred from repeated player observations and community discussions.

---

## Core Idea

We propose that every player may have a hidden numerical value:

B = Hidden Break Balance  
S = Current Table Stake

The table stake determines how much Break Credit is added or removed.

### Proposed Rule

At the start of the match:

- You receive the break → `B = B - S`
- Opponent receives the break → `B = B + S`

At the end of the match:

- You win → `B = B + S`
- You lose → `B = B - S`

This produces four basic states:

| Situation | Change |
|---|---:|
| Opponent breaks + You win | **+2S** |
| You break + You win | **0** |
| You break + You lose | **-2S** |
| Opponent breaks + You lose | **0** |

---

# Example: 1 Million Table

If:

`S = 1,000,000`

and the opponent receives the break and you win:

`+1,000,000` because the opponent received the break  
`+1,000,000` because you won  

Total:

`B = +2,000,000`

This theoretically equals the value of **two breaks on the same 1M table**.

---

## Break + Win

If you receive the break and win:

`-1M + 1M = 0`

The break cost is balanced by the win.

---

## Break + Loss

If you receive the break and lose:

`-1M -1M = -2M`

This produces a strong negative Break Balance.

This may explain why after receiving the break and losing, a player can move to a lower table and still not receive the next break.

---

# Why Changing Tables Matters

The theory proposes that the hidden balance may remain attached to the account when changing tables.

Example:

`B = +2,000,000`

At a 1M table:

`2M / 1M = 2 break units`

At a 500K table:

`2M / 500K = 4 break units`

At a 100K table:

`2M / 100K = 20 break units`

Therefore a positive value earned on a high-stake table becomes much larger relative to a lower-stake table.

This could explain what players have historically called the:

- Break Trick
- Due for the Break
- Break Algorithm
- Break Assignment
- Break Selection
- Break Priority
- Break History
- Hidden Break Credit
- Break Balance
- Stateful Break System
- Weighted Break System
- Matchmaking Break
- Break Sequence
- Break RNG
- Coin-Toss Theory

---

# Possible Break Priority Formula

The balance itself may not directly determine who receives the break.

A possible second-stage variable is:

`Break Priority = B / Current Stake`

The matchmaking system could then compare both players.

Conceptually:

Matchmaking  
↓  
Read Player A Break Balance  
Read Player B Break Balance  
↓  
Divide by current stake  
↓  
Compare Break Priority  
↓  
Apply additional RNG / hidden conditions  
↓  
Assign the break

The exact decision layer is still unknown.

---

# Zero-Sum Property

One interesting feature of this model is that it can be zero-sum.

If Player A receives the break and loses:

Player A = `-2S`

The opponent:

Player B = `+2S`

Total:

`0`

This means Break Credit could behave like a hidden value transferred between the two players.

---

# What This Theory Explains

The model may explain why:

- break assignment does not behave like strict alternation;
- the same player can receive multiple breaks;
- a player can go several matches without a break;
- break state appears to survive table changes;
- winning when the opponent had the break appears especially valuable;
- receiving the break and losing appears especially damaging;
- high-stake matches appear to create stronger effects than low-stake matches;
- the community's "Break Trick" sometimes appears to work.

---

# The Central Formula

### Opponent breaks + Win

`+2S`

### You break + Win

`0`

### You break + Lose

`-2S`

### Opponent breaks + Lose

`0`

Where:

`S = Current Table Stake`

and:

`B = Hidden Break Balance`

---

# What Is Still Unknown

We still do not know:

1. Whether Miniclip actually stores a hidden Break Balance.
2. Whether the value is exactly equal to the stake.
3. Whether table stakes are converted into internal weights.
4. Whether Break Balance has a maximum or minimum.
5. Whether the value decays over time.
6. Whether closing the game affects it.
7. Whether game modes use different systems.
8. Whether the opponent's history is compared directly.
9. How much RNG is involved.
10. Whether additional variables exist.

---

# How To Test It

Players can record consecutive matches with:

- Table stake
- Who received the break
- Win or loss
- Previous table stake
- New table stake
- Predicted Break Balance
- Who received the next break

The important point is to record **all consecutive matches**, not only matches that support the theory.

---

# Current Status

**Community-derived hypothesis — not confirmed Miniclip code.**

The purpose of this repository is to make the model:

- public;
- testable;
- falsifiable;
- reproducible;
- open to improvement.

If you have recorded match sequences that support or contradict this model, please open a GitHub Issue and share the data.

---

## Search Terms

8 Ball Pool Break Algorithm  
8 Ball Pool Break Trick  
8 Ball Pool Hidden Break System  
8 Ball Pool Break Priority  
8 Ball Pool Break Assignment  
8 Ball Pool Break Balance  
8 Ball Pool Break Credit  
8 Ball Pool Due For The Break  
8 Ball Pool Break RNG  
8 Ball Pool Matchmaking Break  
Hidden Break Credit Theory  
HBCT

---

## Disclaimer

8 Ball Pool and Miniclip are trademarks of their respective owners.

This repository is an independent community research hypothesis and is not affiliated with, endorsed by, or based on leaked private code from Miniclip.
