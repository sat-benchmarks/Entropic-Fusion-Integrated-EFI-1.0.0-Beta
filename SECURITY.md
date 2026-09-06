# Security Research and Vulnerability Reporting

EFI 1.0.0-beta.7 is intentionally published for cryptanalysis and security research.

Researchers are expressly permitted under the accompanying licence to inspect, reverse engineer, instrument, fuzz, benchmark, modify for research, and cryptanalyse the software and its file formats, and to publish reproducible findings.

## Research findings versus implementation vulnerabilities

A cryptanalytic result that challenges a published research claim may be published directly. For implementation vulnerabilities that could expose users' plaintext, keys, identities or hidden profiles, coordinated disclosure before publication is appreciated so that a corrective build can be prepared.

## Useful report contents

Please include the exact EFI version, operating system/build environment, affected component, minimal reproduction, expected behaviour, observed behaviour, exploit/attack code where practical, and whether the issue requires local access, a malicious container, a chosen input, secret material, or an oracle.

## Scope boundaries already documented

The current B.23.1 raw-KEM-secret oracle limitation is known and documented. EFIPRIV4 duress erasure is scoped to the current container copy and does not claim to erase backups, snapshots, filesystem journals, SSD remanence, cloud version history or prior copies.

## No retaliation for bona fide research

Bona fide security research conducted within the licence terms is an intended use of this public beta.
