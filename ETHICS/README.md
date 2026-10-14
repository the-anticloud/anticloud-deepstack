# Ethics — DEEPSTACK

**Project:** DEEPSTACK  
**Category:** SURVEILLANCE_CAMERA  
**Upstream:** see BENCH.json  
**Pinned commit:** `73b6f7ab0f9a8acc8f7a49c6f13594fe470de042`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `1ce060e6c796dc47ef65c04dfa99082863b8c339b0b8e6e3c0346e9f4170c705`  
**Date:** October 2026

## Position

DEEPSTACK is packaged for offline deployment with a verifiable audit trail. The
ethical questions this raises are answered by making the system's behaviour
checkable rather than by policy statements.

## The four commitments

1. **No hidden egress.** The deployment has no external API dependency; this is
   testable by running it with the network disconnected.
2. **Attributable output.** Every artifact is recorded in a hash chain, so what
   the system produced can be reconstructed.
3. **Operator control.** The institution owns the hardware and the keys.
4. **Refusal to overclaim.** Where a certification is not held, the project says
   so rather than implying it.

## Dual use

This project is packaged for civilian and public-sector deployment. Where an
upstream has dual-use characteristics, the licence gate and the reference-only
marking in `BENCH.json` record that.
