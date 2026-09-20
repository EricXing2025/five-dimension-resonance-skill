---
name: five-dimension-resonance
description: Analyze BTC and major crypto assets with a Five-Dimension Resonance swing framework using 1D for regime and 4H for execution. Covers trend/space, volatility, volume/flow, momentum/divergence, and time/Ichimoku. Produces two-sided scenarios, triggers, invalidation levels, and risk-first execution states.
---

# Five-Dimension Resonance Skill

## Purpose

Use this skill to evaluate BTC or other liquid crypto assets on a **1D + 4H swing horizon**.

The framework is designed around a common late-trend sequence:

**Top 1 → pullback/retest → possible Top 2 → mean reversion**

This is a scenario framework, not a prophecy. Never assume a double top must happen.

## Safety Boundary

This skill is research and decision support, not an order-execution system or a
guarantee of profit. Do not place, modify, cancel, or widen orders based only
on this skill's output. Treat every scenario as conditional on the stated data,
trigger, and invalidation; when the required data is unavailable, remain
fail-closed and request it.

## Core Principles

1. **1D decides the regime. 4H decides execution.**
2. Use **confluence**, not single-indicator triggers.
3. A moving average is an observation tool, not a force field.
4. Price structure and invalidation always outrank narrative.
5. If data is missing, say so. Never fabricate indicator values.
6. Always produce at least two scenarios: continuation/rebound and failure/breakdown.
7. Every actionable idea must include an explicit invalidation condition.
8. Never recommend removing or widening a stop merely because price moved against the position.

## Required Inputs

Preferred:
- Symbol, e.g. BTCUSDT
- 1D OHLCV data
- 4H OHLCV data

Optional precomputed indicators:
- BBI(3,6,12,24)
- MA30
- Bollinger Bands(20,2)
- VR(26), VR MA(6)
- OBV, OBV MA(20)
- RSI(14)
- MFI(14)
- CCI(14)
- Ichimoku(9,26,52,26)

If indicators are not provided but OHLCV is available, calculate them. If neither OHLCV nor indicator values are available, request data instead of guessing.

# Dimension 1 — Space & Trend

## BBI
Parameters: MA3, MA6, MA12, MA24.

BBI = average of MA3, MA6, MA12, MA24.

Interpretation:
- Primary short/mid-term support reference during an uptrend.
- Watch for the **first meaningful retest** after an extended move.
- A 4H lower wick/rejection near BBI can support a rebound thesis.

## MA30
Interpretation:
- Medium-term trend slope and mean-reversion anchor.
- Rising MA30 supports an uptrend regime.
- Do not state that rising MA30 prevents a sharp selloff.

Record:
- price vs BBI
- distance to BBI (%)
- MA30 slope
- price vs MA30
- distance to MA30 (%)

# Dimension 2 — Volatility & Channel

## Bollinger Bands
Parameters: Length 20, StdDev 2.

Focus on band geometry:
- upper band flattening
- lower band rising
- bandwidth contraction/expansion

Interpretation:
- Upper band flattening + lower band rising often suggests trend deceleration and transition toward a high-level range.
- Rejection from a flat upper band during a second push can strengthen a distribution / Top 2 scenario.

Do not use “touch upper band = short” or “touch lower band = long” mechanically.

# Dimension 3 — Volume & Positioning

## VR
Parameters: VR 26, MA 6.

Use VR to judge short-term participation and heat.

## OBV
Parameters: OBV, OBV MA20.

Interpretation:
- Price pulls back while OBV remains stable/high: compatible with rotation or profit-taking.
- OBV breaks below its MA while VR deteriorates: raises the probability that the pullback is becoming a larger trend failure.

Flag as **high-risk invalidation context** when:
- OBV loses OBV MA
- participation deteriorates materially
- price also loses structural support

Do not use an isolated VR threshold as a standalone exit.

# Dimension 4 — Momentum & Divergence

## RSI(14) / MFI(14)
Primary use: compare Top 1 vs Top 2.

Look for bearish divergence:
- price equal/higher
- RSI/MFI materially lower than the prior peak

A divergence is stronger when it coincides with:
- prior high/resistance
- flat Bollinger upper band
- weakening volume participation

## CCI(14)
Use the “first retest” idea carefully.

A first decline from strong overbought conditions toward +100 / 0 can support a mean-reversion rebound **only when**:
- 1D regime remains constructive
- price is near BBI/structural support
- 4H shows rejection/stabilization

Never use CCI alone as an entry trigger.

# Dimension 5 — Time & Ichimoku

Parameters: 9,26,52,26.

Use:
- future cloud thickness/expansion
- Chikou Span interaction with historical price/cloud zones
- likely time windows where the current range structure may mature

Treat time windows as **context**, not exact prediction.

Never claim:
- “the market must reverse on date X”
- “the cloud guarantees support”

Instead say:
- “the current structure has a higher need to resolve within this window”
- “failure to expand before the time window weakens the continuation thesis”

# Four-Stage State Machine

## Stage 1 — Top 1 / Trend Deceleration
Typical evidence:
- new swing high
- upper Bollinger band flattening
- VR cools after a peak
- OBV remains relatively stable

Default stance: stop chasing and wait for pullback structure.

## Stage 2 — Pullback / Retest
Typical evidence:
- price approaches 1D BBI
- MA30 still rising
- 4H prints lower wick/reclaim/stabilization
- CCI reaches first key retest area
- OBV does not show obvious distribution

Potential action: only consider a rebound trade after 4H confirmation.

## Stage 3 — Top 2 / Distribution Test
Typical evidence:
- price returns to prior high/resistance
- double top or false breakout
- RSI/MFI bearish divergence
- rejection near flat Bollinger upper band
- participation weaker than Top 1

Potential action: prioritize profit-taking. Only consider short exposure after right-side confirmation.

## Stage 4 — Mean Reversion / Trend Repair
Typical evidence:
- high-level range loses structure
- price migrates toward MA30
- OBV/VR weaken
- support reclaim attempts fail

Default stance: reduce directional conviction, avoid “it must bounce” logic, reassess regime after MA30 interaction.

# Long Entry Checklist

A long setup is stronger when most are true:
- [ ] 1D trend remains constructive
- [ ] MA30 slope > 0
- [ ] price is near 1D BBI / structural support
- [ ] 4H shows rejection, lower wick, reclaim, or base
- [ ] OBV remains healthy relative to OBV MA
- [ ] no obvious abnormal distribution volume
- [ ] CCI is at a first meaningful retest zone
- [ ] time structure still allows a rebound / second push

Do not require every box mechanically. Explain which boxes matter most in the current regime.

# Invalidation & Risk Rules

Hard invalidation examples:
1. 1D body closes materially below BBI; use roughly 1.5%–2.0% as a reference band, not a universal constant.
2. Price loses the defining 4H rejection low.
3. OBV loses its MA and participation deteriorates.
4. Market structure changes from higher-low behavior to a confirmed lower-low sequence.

Risk rules:
- Never advise cancelling a predefined stop because of hope.
- Never widen a stop solely to avoid realizing a loss.
- If the thesis is invalid, say: **THESIS INVALIDATED**.

# Profit-Taking Logic

Prioritize exits when several appear together:
- prior high/predefined target reached
- Top 2/double-top structure
- RSI/MFI bearish divergence
- flat upper Bollinger rejection
- weakening volume participation
- time window is mature
- failed breakout/failed acceptance above resistance

Avoid demanding the exact top.

# Analysis Workflow

## Step 1 — Verify Data
Report:
- symbol
- data timestamp
- 1D data availability
- 4H data availability
- missing indicators

## Step 2 — Regime
Classify:
- strong trend
- trend deceleration
- high-level range
- breakdown / mean reversion

## Step 3 — Evaluate Each Dimension
Do **not** create a fake numerical confidence score.

Use:
- Bullish
- Neutral
- Bearish
- Mixed

Evaluate:
1. Space / trend
2. Volatility
3. Volume / flow
4. Momentum
5. Time

## Step 4 — Identify Current Stage
Pick:
- Stage 1
- Stage 2
- Stage 3
- Stage 4
- Unclear / transition

Explain why.

## Step 5 — Build Two Scenarios

### Scenario A — Continuation / Rebound
Include:
- trigger
- confirmation
- target area(s)
- invalidation

### Scenario B — Failure / Breakdown
Include:
- trigger
- confirmation
- downside area(s)
- invalidation

## Step 6 — Execution View
Return one of:
- WAIT
- WATCH LONG
- LONG CONFIRMED
- TAKE PROFIT / REDUCE
- WATCH SHORT
- SHORT CONFIRMED
- THESIS INVALIDATED

Only use CONFIRMED when the stated trigger has actually occurred.

# Output Format

## Five-Dimension Snapshot
**Symbol:**
**Timeframe:** 1D regime + 4H execution
**Data timestamp:**
**Current stage:**

### 1. Space / Trend
- BBI:
- MA30:
- Key support:
- Key resistance:
- Read:

### 2. Volatility
- Boll structure:
- Read:

### 3. Volume / Flow
- VR:
- OBV:
- Read:

### 4. Momentum
- RSI:
- MFI:
- CCI:
- Divergence:
- Read:

### 5. Time
- Ichimoku:
- Time-window read:

## Scenario A — Continuation
**Trigger:**
**Confirmation:**
**Targets:**
**Invalidation:**

## Scenario B — Failure
**Trigger:**
**Confirmation:**
**Downside areas:**
**Invalidation:**

## Execution
**Status:** WAIT / WATCH LONG / LONG CONFIRMED / TAKE PROFIT / REDUCE / WATCH SHORT / SHORT CONFIRMED / THESIS INVALIDATED

**What would change my mind:**
1.
2.
3.

# Tone Rules

- Write like a professional trader/researcher, not a hype account.
- Use probability language: “supports”, “raises/lowers the probability”, “compatible with”, “needs confirmation”.
- Avoid: “必涨”, “必中”, “绝对不会跌”, “庄家一定在……”, “100%”.
- Separate observation from inference.
- If evidence conflicts, explicitly say **Mixed**.

# Example Invocation

Analyze BTCUSDT with the Five-Dimension Resonance framework.

Requirements:
1. Use 1D to determine regime and 4H for execution.
2. Calculate BBI(3,6,12,24), MA30, Boll(20,2), VR(26), VR MA(6), OBV/OBV MA20, RSI14, MFI14, CCI14, Ichimoku(9,26,52,26).
3. Identify the current four-stage state.
4. Give both continuation and breakdown scenarios.
5. State exact trigger and invalidation conditions.
6. Do not assume a double top must form.
7. Do not invent missing data.
8. End with an execution status.
