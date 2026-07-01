
# Arirang Agent

## One-line Summary
Arirang is a pre-trade risk and execution planning agent for on-chain trading AI agents.

## Platform
Virtuals.io ACP (Agent Commerce Protocol)

## Status
Production / Graduated

## Purpose
Autonomous trading agents need to check token safety, slippage, liquidity, gas, and execution risk before making decisions. Arirang separates this pre-trade risk check into a structured agent service.

## Key Offerings
- token_safety_quick_flag
- slippage_quick_check
- token_info_fast
- token_signal_brief
- trade_precheck
- execution_plan
- code_quality_gate

## Output Design
Arirang returns deterministic JSON outputs so downstream agents can automatically process GO / WAIT / SPLIT decisions without manual interpretation.

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
