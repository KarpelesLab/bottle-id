# Bottle and IDCard Protocol Specification

This repository contains the IETF Internet-Draft specification for the Bottle and IDCard protocols.

## Overview

**Bottle** is a secure message container protocol that provides:
- Multi-recipient encryption using AES-256-GCM
- Multiple digital signatures
- Recursive nesting for complex security arrangements (sign-then-encrypt, multi-layer encryption)
- Support for both CBOR and JSON encodings

**IDCard** is a cryptographic identity protocol that provides:
- Purpose-specific subkeys (signing, encryption, authentication)
- Key expiration and revocation
- Verifiable group memberships
- Self-signed identity containers

These protocols bridge the gap between JWT (limited to single signatures), COSE (separate structures without built-in nesting), and PGP (comprehensive but complex).

## Documents

- `draft-karpeles-bottle-idcard-01.xml` - RFCXML source
- `draft-karpeles-bottle-idcard-01.txt` - Generated text format

## Building

To regenerate the text document from the XML source:

```bash
xml2rfc draft-karpeles-bottle-idcard-01.xml
```

Requires [xml2rfc](https://pypi.org/project/xml2rfc/) to be installed.

## Reference Implementation

A reference implementation in Go is available at:
https://github.com/KarpelesLab/cryptutil

## Status

This is an individual submission Internet-Draft. The current version is -01.

## Author

Mark Karpeles <mark@klb.jp>
Karpeles Lab Inc.
https://klb.jp

## License

This Internet-Draft is subject to the IETF Trust Legal Provisions (TLP).
