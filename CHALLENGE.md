# EFI Public Cryptanalysis Challenge

## Don’t believe it. Break it.

Entropic Fusion Integrated (EFI) is being released publicly so that its claims can be tested rather than accepted on trust.

The most useful result is a **reproducible attack**. A successful attack should identify the exact version, inputs, environment, method, expected result and observed result. Code, scripts, traces and minimal reproductions are strongly encouraged.

## Primary attack targets

1. Recover protected plaintext without the legitimate recipient secrets.
2. Reconstruct the B.23.1 Entropic Fusion root key without satisfying the intended private recovery dependencies.
3. Demonstrate a practical bypass of one or both root ML-KEM sessions that still yields the legitimate root key.
4. Find an attack on the Entropic relation substantially below its naive structural counting space.
5. Produce an algebraic, SAT/SMT, meet-in-the-middle, symmetry or structural shortcut against the 4D n=3 Entropic root.
6. Exploit the documented raw-KEM-secret oracle limitation in a stronger practical attack.
7. Recover protected metadata that EFIPRIV3 claims to keep inside the encrypted control region, such as original filename, exact source size, recipient fingerprint, Entropic mode or chain profile.
8. Distinguish an EFIPRIV4 cover-only container from one containing an active hidden profile using public container bytes alone, beyond the documented coarse public geometry.
9. Recover the hidden profile from the **current container copy** after a successful duress event without relying on a backup, snapshot, journal or prior copy.
10. Show that an unrelated wrong credential causes destructive hidden-profile behaviour.
11. Find a shortcut through Standard/Tetration/Pentation state evolution or Entropic Chain that invalidates a documented sequential-dependency claim.
12. Trigger plaintext disclosure, key disclosure, authentication bypass, unsafe parser behaviour or state confusion through malformed, truncated or corrupted containers.
13. Demonstrate a cross-mode or cross-context substitution that produces a legitimate recovery under the wrong transcript, identity, mode or application context.
14. Find a practical key/material exposure in memory, temporary files, logs or the Windows vault-host boundary that defeats an EFI security claim.

## Known limitation is not a prize discovery

B.23.1 already records that if an external oracle hands an attacker **both raw root ML-KEM shared secrets**, the current EF-gated session contribution can be recomputed from those secrets plus public commitment/transcript material. The current root therefore does not claim an independently necessary third Entropic secret under that oracle model.

That limitation is public. Find something worse.

## What does not count as breaking EFI

- Pointing out that raw search-space size is not equivalent to security bits. The project already says this.
- Pointing out that ML-KEM is key encapsulation rather than bulk encryption. The documentation already makes that distinction.
- Pointing out that backups, snapshots, cloud history or filesystem journals may preserve pre-duress material. The duress claim is deliberately scoped to the current container copy.
- Merely replacing the program binary with a modified program that ignores checks, unless the modification demonstrates a security property that the official build claims to enforce against a local attacker.

## Reporting

Public write-ups are welcome. If a finding may expose users to an implementation vulnerability rather than merely challenge a research claim, see [SECURITY.md](SECURITY.md) for coordinated-reporting guidance.

The project welcomes negative results too: failed attack methods, solver encodings, benchmark data and structural observations can all help define the actual research problem.
