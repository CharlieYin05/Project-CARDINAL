# Project CARDINAL

**Contactless Authentication Research, Development, and NFC Integration Lab**

> An experimental, cross-disciplinary project exploring RFID/NFC smart cards, secure authentication, Android Host Card Emulation (HCE), and high-performance computing.

## Overview

Project CARDINAL began with a practical question: **can a smartphone offer a convenient, secure alternative to carrying a physical contactless credential?**

Answering that question involves more than reading a card's identifier. This project investigates the full stack—from radio communication and smart-card protocols to cryptographic authentication, mobile operating-system constraints, and computational performance.

The goal is to **understand and document what is technically possible**, build reproducible prototypes in a controlled lab, and explain the security boundaries that prevent arbitrary credential cloning.

**Status:** Early research and prototyping. Features described below are goals unless explicitly marked as implemented.

## Research Areas

| Area | Focus |
| --- | --- |
| RFID / NFC | 13.56 MHz communication, ISO/IEC 14443, card identification and protocol analysis |
| Smart cards | ISO-DEP, APDUs, DESFire-family architecture, application/file concepts |
| Cryptography | AES-128, mutual authentication, challenge-response, session-key concepts |
| Android | Kotlin, NFC APIs, `HostApduService`, Host Card Emulation and hardware limitations |
| High-performance computing | Parallel programming, cryptographic throughput benchmarking and key-space analysis |
| Systems integration | Reproducible experiments, interoperability testing and technical documentation |

## Hardware and Software

**Planned / available research equipment**

- Proxmark3 Easy-compatible device for RFID/NFC analysis
- NFC-capable Android smartphone for reader-mode and HCE experiments
- Self-owned NFC tags, development smart cards, and a test reader
- Authorized CPU/GPU compute resources for benchmarking

**Development tools**

- Proxmark3 client / Iceman firmware (subject to hardware compatibility)
- Android Studio, Kotlin, Android NFC APIs
- Python and C/C++ for analysis and test utilities
- Slurm and GPU programming tools where available and authorized
- Git for version control and reproducibility

## Project Roadmap

- [ ] **Phase 1 — Hardware bring-up:** identify Proxmark3 hardware/firmware, validate the HF antenna, and document read-only card discovery.
- [ ] **Phase 2 — Smart-card fundamentals:** study ISO 14443-4 and APDU exchanges using lab-owned cards and readers.
- [ ] **Phase 3 — Authentication laboratory:** implement and test challenge-response flows with independently generated test keys.
- [ ] **Phase 4 — Android HCE prototype:** create a Kotlin application that responds to custom APDUs and interoperates with a controlled reader.
- [ ] **Phase 5 — Compute experiments:** benchmark cryptographic workloads on authorized CPU/GPU resources; analyze performance and key-space growth.
- [ ] **Phase 6 — Integration and findings:** document compatibility, limitations, threat models, and reproducible results.

## Proposed Repository Structure

```text
CARDINAL/
├── android/          # Android HCE application
├── firmware-notes/   # Proxmark3 hardware and firmware observations
├── protocols/        # APDU examples and protocol notes
├── crypto-lab/       # Authentication demos using test keys
├── benchmarks/       # CPU/GPU benchmark code and results
├── docs/             # Research notes, diagrams and reports
└── README.md
```

*This layout is planned and may change as development progresses.*

## Success Criteria

A successful outcome does **not** require cloning an existing access card. Useful outcomes include:

1. Identifying and explaining the relevant NFC protocol layers.
2. Demonstrating authentication with credentials and keys controlled by the project.
3. Building a functional Android HCE proof of concept.
4. Measuring cryptographic performance with reproducible benchmarks.
5. Documenting why some contactless systems cannot be replicated by ordinary phone NFC APIs.

## Responsible Research

This project is intended for education, defensive security research, and authorized interoperability testing.

- Only conduct active testing on equipment and credentials you own or are explicitly authorized to assess.
- Do not attempt to recover, clone, or bypass third-party access credentials.
- Keep real credential identifiers, cryptographic secrets, and sensitive traces out of the repository.
- Use synthetic datasets and independently generated keys in all published examples.
- Follow the applicable rules of shared computing infrastructure and responsible disclosure practices.

## Documentation and Results

Experiment notes, setup instructions, benchmark methodologies, and validated results will be added as they become available. Claims will be distinguished from hypotheses and clearly labeled with hardware, software, and test conditions.

## License

License to be determined. Until a license is added, no permission to reuse the code is granted by default.

---

**Project CARDINAL — exploring the boundary between contactless convenience and cryptographic trust.**
