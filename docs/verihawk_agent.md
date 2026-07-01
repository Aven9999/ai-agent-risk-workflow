# VeriHawk Agent

## One-line Summary
VeriHawk is a post-execution trust and audit support agent for AI-to-AI workflows.

## Platform
Virtuals.io ACP (Agent Commerce Protocol)

## Status
Sandbox

## Purpose
After an autonomous agent executes a trade or on-chain action, the result needs to be verified against predefined conditions such as slippage, position size, fee sanity, and policy constraints.

## Key Offerings
- proof_ping_quick
- proof_bundle_standard
- policy_compliance_verdict
- execution_audit_report

## Output Design
VeriHawk returns structured JSON outputs that can be used for proof readiness, compliance verdicts, and execution audit reports.

## Example Output
```json
{
  "status": "COMPLETED",
  "verdict": "DENY",
  "checks": {
    "position_size": "EXCEED",
    "slippage_constraint": "PASS",
    "deny_list": "PASS"
  },
  "remediation_hints": [
    "reduce_position_size_below_threshold"
  ]
}
