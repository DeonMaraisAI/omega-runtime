# How to Verify Omega Runtime

Omega Runtime is a local reproducibility demo.

It verifies whether the files inside the reproducible bundle still match their recorded hashes.

## Requirements

```text
Python 3
```

## Steps

1. Download `omega_reproducible_bundle.zip` from the repository.
2. Extract the ZIP into a local folder.
3. Open a terminal in the extracted folder.
4. Run:

```bash
python verify_rebuild.py
```

## Expected result

If no protected file has changed, verification should pass.

If any protected file has changed, verification should fail.

## Tamper test

After one passing run:

1. Edit any protected file inside the extracted bundle.
2. Save the file.
3. Run:

```bash
python verify_rebuild.py
```

Expected result:

```text
verification fails
```

## Boundary

This verifies local reproducibility and tamper detection only.

It does not prove:

```text
Bell₂ witness
ACCEPT_SHARED
quorum authority
network propagation
network truth
```

## Correct language

Use:

```text
This bundle verifies whether its files still match the recorded hashes.
```

Do not use:

```text
This file verifies itself.
```
