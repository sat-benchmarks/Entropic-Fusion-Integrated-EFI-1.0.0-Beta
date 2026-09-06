# Entropic Fusion Integrated (EFI)

## Public Cryptanalysis Beta

EFI 1.0.0-beta.7 is an experimental research cryptography system released for independent inspection, reverse engineering and cryptanalysis.

**Experimental research software. Not formally certified.**

### What Entropic Fusion means

```text
Entropic Notation + ML-KEM-768 + ML-KEM-1024 = Entropic Fusion

Entropic Fusion
+ Entropic Tetration / Pentation
+ Entropic Chain / EC100
+ AES-256-GCM authenticated data encryption
+ metadata-private streaming and graduated padding
+ optional deniable storage and deliberate duress
= EFI
```

Entropic Fusion is intended as a coupled root, not a stack of detachable cryptographic layers. In the legitimate recovery path, the Entropic witness gates recovery of the wrapped root ML-KEM private material, and the resulting KEM sessions participate in the same root derivation.

The current B.23.1 implementation has a documented limitation: if an external oracle supplies both raw root ML-KEM shared secrets, the current EF-gated session contribution can be recomputed from those secrets plus public transcript and commitment material. EFI therefore does not claim that the current root formally proves an independently necessary third Entropic hardness source under that oracle model.

### Why HNDL matters

HNDL means **Harvest Now, Decrypt Later**. An adversary can collect encrypted material today and retain it in the hope that future quantum computers or other cryptanalytic advances will later defeat the public-key mechanism that protected its keys.

EFI uses NIST-standardised ML-KEM for post-quantum key establishment while AES-256-GCM protects the actual file data. The novel Entropic constructions are experimental and are being released specifically so they can be attacked.

## Public challenge

**Do not trust the claims. Test them.**

See [CHALLENGE.md](CHALLENGE.md) for concrete attack targets.

## Files in this repository

- `README.md` — project and architecture overview
- `LICENSE` — Public Cryptanalysis Evaluation Licence
- `CHALLENGE.md` — attack targets
- `SECURITY.md` — reporting guidance
- `ENTROPIC_FUSION_DEFINING_PAPER.pdf` — defining architecture paper
- `EFI_1.0.0-beta.5_SOURCE.zip` — compact source archive for inspection and cryptanalysis
- `SHA256SUMS.txt` — hashes for the repository artefacts

Compiled Windows binaries are published separately as GitHub **Release assets**. The normal public downloads are the Windows installer and portable ZIP. Standalone `EntropicFusionIntegrated.exe` and `EntropicFusionHost.exe` may also be attached for direct binary analysis.

`EntropicFusionHost.exe` is the separate vault-host process used by the WinFsp-backed encrypted vault architecture.

## Licence

This is not an OSI open-source release. Security research, reverse engineering, cryptanalysis and publication of reproducible findings are expressly permitted under the licence. Commercial exploitation, resale and rebranding are reserved.
