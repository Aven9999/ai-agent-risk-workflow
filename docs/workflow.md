# AI Agent Risk Workflow

## Concept

This project summarizes a pre-trade and post-execution risk workflow for AI agents.

The goal is not to automate trading decisions blindly, but to separate risk checkpoints into structured outputs that downstream agents can consume.

## Workflow

```text
External Trading Agent
→ Arirang: token info / token safety / slippage check / trade precheck / execution plan
→ Execution
→ VeriHawk: proof readiness / proof bundle / policy compliance / execution audit
