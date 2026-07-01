# VeriHawk Agent

## One-line Summary

VeriHawk is a post-execution trust and audit support agent for AI-to-AI workflows.

## Platform

Virtuals.io ACP (Agent Commerce Protocol)

## Status

Sandbox

## Purpose

After an autonomous agent executes a trade or on-chain action, the result needs to be verified against predefined conditions such as slippage, position size, fee sanity, and policy constraints.

VeriHawk separates this post-execution verification process into structured agent services.

## Key Offerings

- proof_ping_quick
- proof_bundle_standard
- policy_compliance_verdict
- execution_audit_report

## Recommended Flow

```text
proof_ping_quick
→ proof_bundle_standard
→ policy_compliance_verdict
→ execution_audit_report
```

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
```

## Product Learning

This project helped me understand the importance of post-execution verification, auditability, standardized output formats, and risk-control workflows.

## Connection to Crypto Product Strategy

A similar approach can be applied to user-facing investment services such as:

- Risk alerts
- Policy-based warnings
- Transaction review
- Investor protection features
- Post-action verification and audit logs
