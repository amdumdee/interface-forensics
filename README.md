# Interface Forensics

A reproducible evidence corpus for deceptive and manipulative interface patterns.

The project separates:

**source → candidate → interface evidence → classification → counter-check → status**

A source may identify a candidate. The interface itself is the evidence. A taxonomy provides the classification vocabulary. The counter-check determines whether the classification survives scrutiny.

## Repository principles

1. **Tier 2 sources are leads, not facts.**
2. **Capture the interface, not the poster's interpretation.**
3. **Classify against a defined pattern type.**
4. **Record the counter-check.**
5. **Do not infer motive when observable behavior is sufficient.**
6. **If evidence is unresolved, use `candidate-uncertain`.**
7. **One instance = one evidence record.**
8. **Preserve timestamps and reproduction context.**
9. **Keep taxonomy, evidence, and interpretation separate.**
10. **A disliked interface is not automatically a deceptive interface.**

## Directory structure

```text
interface-forensics/
├── taxonomy/
├── instances/
│   ├── confirmed/
│   ├── candidate-uncertain/
│   └── rejected/
├── evidence/
│   ├── screenshots/
│   ├── recordings/
│   └── captures/
├── sources/
│   ├── authoritative/
│   ├── regulatory/
│   └── academic/
├── methodology/
└── reports/
    ├── monthly/
    └── annual/
```

## Evidence pipeline

```text
SOURCE
  ↓
CANDIDATE
  ↓
CAPTURE INTERFACE
  ↓
EVIDENCE
  ↓
CLASSIFY
  ↓
COUNTER-CHECK
  ↓
CONFIRMED / CANDIDATE-UNCERTAIN / REJECTED
```

## Status definitions

- `candidate-uncertain`: evidence exists but classification remains unresolved.
- `confirmed`: defined criteria are met and counter-checks are resolved.
- `rejected`: evidence was reviewed and the pattern definition was not met.

## Evidence standard

Every confirmed instance should have:

- exact interface/product identification
- URL or other source locator
- capture timestamp
- screenshot or recording
- exact relevant interface text
- reproduction steps where possible
- taxonomy mapping
- explicit qualification reasoning
- counter-check
- authoritative source supporting the pattern type

## Important distinction

**Observed fact:** what the interface actually displays or does.

**Classification:** which defined pattern type the behavior matches.

**Interpretation:** what the mechanism may mean from a security/social-engineering perspective.

Do not collapse these into one claim.

## Scope

This project is intended as a research and evidence corpus. It is not a legal determination that a company violated a law or regulation.
