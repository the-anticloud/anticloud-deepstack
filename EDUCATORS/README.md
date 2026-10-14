# Educators — DEEPSTACK

**Project:** DEEPSTACK  
**Category:** SURVEILLANCE_CAMERA  
**Upstream:** see BENCH.json  
**Pinned commit:** `73b6f7ab0f9a8acc8f7a49c6f13594fe470de042`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `1ce060e6c796dc47ef65c04dfa99082863b8c339b0b8e6e3c0346e9f4170c705`  
**Date:** October 2026

## Teaching with DEEPSTACK

The project is usable as a worked example of offline-first packaging with a
cryptographic audit chain. It ships with the assurance suite, the evidence
register and the ledger, so students can verify claims rather than take them on
faith.

## Suggested exercises

1. Run `python tools/run_bench.py --out BENCH.json` and read the 16 results.
2. Recompute the SHA3-256 of a row's evidence file and compare to the register.
3. Walk the AIOSS chain from genesis to head `1ce060e6c796dc47ef65c04dfa99082863b8c339b0b8e6e3c0346e9f4170c705` and confirm every link.
4. Break one artifact and observe the chain fail to verify.

## Licence for teaching

Apache 2.0 terms apply to academic and teaching use. See `24_ANTICOMMONS_LICENSE`.
