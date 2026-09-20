# Five-Dimension Resonance Agent Skill

A portable Agent Skill for structured crypto swing analysis. It uses the 1D
chart to determine the regime and the 4H chart to identify execution conditions
across five dimensions: space/trend, volatility, volume/flow,
momentum/divergence, and time/Ichimoku.

## 中文简介

把整个 `five-dimension-resonance-skill` 文件夹交给支持 Skills / Agent
Instructions 的 AI Agent 即可。

最简单的调用方式：

> 使用 five-dimension-resonance skill 分析 BTCUSDT。日线定大方向，4H 找执行点。必须给多空两套场景、触发条件、失效条件，不要只给单边结论。

如果你的 Agent 不支持 Skills 目录，也可以直接把 `SKILL.md` 作为系统提示词或知识文件导入。

## English usage

Give the complete `five-dimension-resonance-skill` folder to an agent that
supports Skills or agent instructions. A minimal prompt is:

> Use the five-dimension-resonance skill to analyze BTCUSDT. Use 1D for the regime and 4H for execution. Provide both continuation and breakdown scenarios with triggers, confirmations, targets, and invalidation conditions.

## Data and scope

- The agent must use real, timestamped market data and must not invent missing indicators.
- The framework is designed for BTC and other liquid crypto assets on a 1D + 4H swing horizon.
- The output is research and decision support, not an automated trading strategy or a profit guarantee.
- Do not place, modify, cancel, or widen an order solely because of this skill's output.

## Files

- `SKILL.md` — the complete skill instructions.
- `README.md` — usage, scope, and release notes.
- `LICENSE` — MIT license.

## License

MIT. See [`LICENSE`](LICENSE).
