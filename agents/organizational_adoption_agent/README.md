# Organizational Adoption Agent

Assignment 7 | MASY1-GC 1800 | Version 0.1 | November 3, 2026

This specialist evaluates organizational readiness for a six-month advisory Agentic AI scheduling pilot in a hypothetical wafer fab. A human explicitly approves every production schedule change. The cases hold material assumptions constant and isolate successful, failed and undocumented manual fallback execution.

From the repository root, use the instructor's workflow:

```sh
agent=agents/organizational_adoption_agent
python tools/check_frozen_core.py
python tools/build_prompt.py --agent "$agent" --case "$agent/cases/primary.json"
python tools/validate_response.py --help
```

Repeat the packet build for `contrast_1.json` and `contrast_2.json`. Submit each complete packet in a fresh ChatGPT conversation. Save the verbatim JSON, then run the supplied validator and inspect the eight domains, evidence classifications, gate decisions and consistency across cases. See the [Agent Record](records/agent_record.md) for findings and evidence status.
