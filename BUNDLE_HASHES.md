# Omega Runtime Bundle Hashes

This file publishes visible integrity references for `omega_reproducible_bundle.zip`.

## Repository ZIP object

```text
FILE: omega_reproducible_bundle.zip
GIT_BLOB_SHA: 095d056ba8c93945eed349c9edbf71e16a9a4d2c
```

## Bundle manifest hash

The bundle contains `manifest.json` with this recorded global hash:

```text
MANIFEST_GLOBAL_HASH: 594f05c1fabbefac8a98acf4fa4918d7a5ba931905ce8e6f69ff940b56d28af4
```

## Meaning

```text
GIT_BLOB_SHA
  identifies the ZIP object as stored in GitHub/Git.

MANIFEST_GLOBAL_HASH
  is the internal reproducibility hash checked by the extracted verifier.
```

## Current boundary

```text
LOCAL_REPRODUCIBILITY: TRUE
TAMPER_DETECTION: TRUE
ACCEPT_SHARED: FALSE
PROPAGATION: BLOCKED
NETWORK_UPDATE: BLOCKED
```

## Verification

To verify the bundle locally:

```bash
unzip omega_reproducible_bundle.zip -d omega-runtime-verify
cd omega-runtime-verify
python verify_rebuild.py
```

Expected pass output:

```text
REPRODUCIBLE VALID
```
