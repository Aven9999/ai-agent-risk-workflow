# Arirang Agent

## One-line Summary

Arirang is a pre-trade risk and execution planning agent for on-chain trading AI agents.

## Platform

Virtuals.io ACP (Agent Commerce Protocol)

## Status

Production / Graduated

## Purpose

Autonomous trading agents need to check token safety, slippage, liquidity, gas, and execution risk before making decisions.

Arirang separates this pre-trade risk check into a structured agent service and returns deterministic JSON outputs so downstream agents can automatically process GO / WAIT / SPLIT decisions without manual interpretation.

## Key Offerings

- token_safety_quick_flag
- slippage_quick_check
- token_info_fast
- token_signal_brief
- trade_precheck
- execution_plan
- code_quality_gate

## Recommended Flow

```text
token_info_fast
→ token_safety_quick_flag
→ slippage_quick_check
→ trade_precheck
→ execution_plan
```

## Example Output

```json
{
  "status": "COMPLETED",
  "decision": "WAIT",
  "slippage_context": {
    "estimated_bps": 142,
    "risk_level": "HIGH"
  },
  "liquidity_context": "insufficient",
  "gas_context": "elevated",
  "recommendation": "split_order_or_wait"
}
```

## Product Learning

This project helped me understand how to design an AI service around user workflow, pricing tiers, deterministic outputs, and risk-based decision routing.

## Connection to Crypto Product Strategy

The same structure can be applied to investment services such as:

- Pre-trade risk alerts
- Watchlist risk checks
- AI-based market briefing systems
- Risk-aware user notification flows
- Structured decision support for high-volatility assets
