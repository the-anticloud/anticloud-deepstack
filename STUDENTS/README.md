# Students — DEEPSTACK

**Project:** DEEPSTACK  
**Category:** SURVEILLANCE_CAMERA  
**Upstream:** see BENCH.json  
**Pinned commit:** `73b6f7ab0f9a8acc8f7a49c6f13594fe470de042`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `1ce060e6c796dc47ef65c04dfa99082863b8c339b0b8e6e3c0346e9f4170c705`  
**Date:** October 2026

## What this project gives you

A complete worked example of offline-first packaging with a cryptographic audit
chain: source pinned at `73b6f7ab0f9a8acc8f7a49c6f13594fe470de042`, a 16-check assurance suite, an evidence register
with per-check hashes, and an AIOSS ledger chain ending at `1ce060e6c796dc47ef65c04dfa99082863b8c339b0b8e6e3c0346e9f4170c705`.

## Learn by verifying

```
python tools/run_bench.py --out BENCH.json
```

Then take any row from `ISOLATED_LAB_RESULTS/03_Result_Register.md`, recompute
the SHA3-256 of its evidence file, and confirm it matches. If it does not match,
the record has been altered — that is the whole point of the chain.

## Licence

Apache 2.0 terms apply to study and teaching use.
