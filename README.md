# Omega Runtime

**If the bundle changes, verification fails.**

This repository ships a reproducible bundle.

The verification contract lives inside `omega_reproducible_bundle.zip`.
The repo README explains how to run it; the verifier checks the extracted bundle files.

## Why pre-validation exists

Internal consistency is required, but never sufficient.

See [PRE_VALIDATION.md](PRE_VALIDATION.md) for upstream false-finality protection.

## How to test

1. Download the zip
2. Extract it
3. Change into the extracted folder
4. Run:

```bash
python verify_rebuild.py
```

Expected result:

```text
REPRODUCIBLE VALID
```

Try to change any file in the extracted bundle and run it again — it will fail.

(Tested with Python 3)

---

No server. No API. No trust required.
