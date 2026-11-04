# Technical audit of preserved Assignment 7 responses

The supplied `tools/validate_response.py` reports PASS on all six original responses. A separate Draft 2020-12 check of the historical responses against `core/output_schema.json` reports five conforming responses and one strict failure. The supplied validator checks required fields and selected types. It does not reject additional root properties.

| Response | Instructor validator | Strict output schema |
|---|---|---|
| v01_primary.json | PASS | PASS |
| v01_contrast_1.json | PASS | PASS |
| v01_contrast_2.json | PASS | PASS |
| v02_primary.json | PASS | PASS |
| v02_contrast_1.json | PASS | PASS |
| v02_contrast_2.json | PASS | FAIL |

The historical failing response contains the unexpected root keys `$schema` and `title`. The frozen schema sets root `additionalProperties` to `false`. The original response remains available in `../responses/v02_contrast_2.json`, and its SHA-256 still matches `run_manifest.md`. Its organizational finding withholds affirmative readiness because witnessed execution evidence is unavailable. That substantive finding does not make the response suitable for strict automated intake.

For team integration, validate each new response against the frozen schema before ingestion. Route a failing response to manual review and retain the original for provenance. No cleaned derivative or replacement run is supplied. Frozen files and the original execution manifest were retained.


## Current version retest

Version 0.3 enumerates the 13 allowed response keys and explicitly excludes schema metadata. The frozen schema, instructor validator and case inputs were retained. The fresh responses `v03_primary.json`, `v03_contrast_1.json` and `v03_contrast_2.json` each passed the instructor validator and complete schema validation with Python jsonschema 4.26.0. The run manifest records the three packet and response hashes.

From the repository root, with jsonschema 4.26.0 available, reproduce the strict check:

```sh
python3 - <<'PYTHON'
import json
from pathlib import Path
from jsonschema import Draft202012Validator

schema = json.loads(Path("core/output_schema.json").read_text())
Draft202012Validator.check_schema(schema)
validator = Draft202012Validator(schema)
responses = Path("agents/organizational_adoption_agent/responses")
for case in ("primary", "contrast_1", "contrast_2"):
    response = responses / f"v03_{case}.json"
    validator.validate(json.loads(response.read_text()))
    print(f"PASS {response}")
PYTHON
```
