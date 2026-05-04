# Omega Runtime

Omega Runtime is a **local reproducibility and tamper-detection demo**.

It is intentionally small.

It proves one public idea:

```text
This bundle verifies whether its files still match the recorded hashes.
```

If a protected file is modified, the local verifier should fail.

## What this proves

```text
LOCAL_REPRODUCIBILITY: TRUE
TAMPER_DETECTION: TRUE
LOCAL_REBUILD_CHECK: TRUE
```

## What this does not prove

```text
BELL2_WITNESS: FALSE
ACCEPT_SHARED: FALSE
QUORUM_AUTHORITY: FALSE
PROPAGATION: BLOCKED
NETWORK_TRUTH: FALSE
```

This repository is not a shared-authority system. It is not a Bell₂ witness. It does not enable network propagation.

## How to test locally

1. Download `omega_reproducible_bundle.zip`.
2. Extract the ZIP.
3. Run:

```bash
python verify_rebuild.py
```

4. Modify any protected file.
5. Run the verifier again.

Expected result:

```text
unchanged files -> verification passes
modified files  -> verification fails
```

## Current boundary

```text
STATUS: LOCAL_REPRODUCIBILITY_DEMO
AUTHORITY: LOCAL_ONLY
ACCEPT_SHARED: FALSE
PROPAGATION: BLOCKED
NETWORK_UPDATE: BLOCKED
```

## No server required

No server. No API. No trust in a website.

The verifier is meant to be run locally against the bundle.
