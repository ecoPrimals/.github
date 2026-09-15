# ecoPrimals

**Sovereign distributed scientific computing in Pure Rust.**

15 composable daemons, 9 validation springs, 98,955 tests, 3.6M lines of Rust.
No C, no cloud, no vendor lock-in. Self-hosted on commodity hardware. AGPL-3.0.

**Live site:** [sporeprint.primals.eco](https://sporeprint.primals.eco) &nbsp;|&nbsp; **Forgejo:** [git.primals.eco](https://git.primals.eco)

---

### What this replaces

| Vendor stack | ecoPrimal |
|---|---|
| AWS/GCP/Azure | Self-hosted [NUCLEUS](https://sporeprint.primals.eco/architecture/nucleus-architecture/) on any Linux box |
| OpenSSL / BoringSSL | [bearDog](https://github.com/ecoPrimals/bearDog) — TLS 1.3, Ed25519, ML-KEM post-quantum, zero C deps |
| Consul / etcd | [songBird](https://github.com/ecoPrimals/songBird) — mDNS, WireGuard overlay, drawbridge proxy |
| S3 / MinIO | [nestGate](https://github.com/ecoPrimals/nestGate) — content-addressed storage, B-tree, journal WAL |
| Kubernetes / Nomad | [biomeOS](https://github.com/ecoPrimals/biomeOS) — deploy graphs, process supervision, Neural API |
| CUDA / ROCm | [barraCuda](https://github.com/ecoPrimals/barraCuda) + [coralReef](https://github.com/ecoPrimals/coralReef) — WebGPU/WGSL, Vulkan f64 |
| Prometheus / Grafana | [petalTongue](https://github.com/ecoPrimals/petalTongue) — egui + ratatui + WASM WebGL |
| Vault / SOPS | [bearDog](https://github.com/ecoPrimals/bearDog) — DPAPI, SecretService, Android Keystore |

### The stack

```
┌─────────────────────────────────────────────────┐
│                    NUCLEUS                       │
│  ┌──────────┐ ┌──────────┐ ┌──────────────────┐ │
│  │ songBird │ │ bearDog  │ │    toadStool     │ │
│  │ network  │ │ identity │ │ GPU/NPU dispatch │ │
│  └──────────┘ └──────────┘ └──────────────────┘ │
│  ┌──────────┐ ┌──────────┐ ┌──────────────────┐ │
│  │ nestGate │ │ biomeOS  │ │    squirrel      │ │
│  │ storage  │ │ nucleus  │ │ AI coordination  │ │
│  └──────────┘ └──────────┘ └──────────────────┘ │
│  ┌──────────┐ ┌──────────┐ ┌──────────────────┐ │
│  │loamSpine │ │rhizoCrypt│ │   sweetGrass     │ │
│  │ lineage  │ │ DAG prov │ │  attribution     │ │
│  └──────────┘ └──────────┘ └──────────────────┘ │
│  ┌──────────┐ ┌──────────┐ ┌──────────────────┐ │
│  │ skunkBat │ │sourDough │ │   petalTongue    │ │
│  │ defense  │ │substrate │ │  visualization   │ │
│  └──────────┘ └──────────┘ └──────────────────┘ │
│  ┌──────────┐ ┌──────────┐ ┌──────────────────┐ │
│  │barraCuda │ │coralReef │ │   plasmidBin     │ │
│  │ GPU math │ │ shaders  │ │  binary depot    │ │
│  └──────────┘ └──────────┘ └──────────────────┘ │
└─────────────────────────────────────────────────┘
```

### Validation springs (175+ papers reproduced)

| Spring | Domain | Tests |
|--------|--------|-------|
| [hotSpring](https://github.com/syntheticChemistry/hotSpring) | Computational physics — lattice QCD, molecular dynamics | 850+ |
| [wetSpring](https://github.com/syntheticChemistry/wetSpring) | Metagenomics, analytical chemistry, mathematical biology | 1,750+ |
| [neuralSpring](https://github.com/syntheticChemistry/neuralSpring) | ML primitives, spectral analysis, structure prediction | 4,500+ |
| [airSpring](https://github.com/syntheticChemistry/airSpring) | Precision agriculture, evapotranspiration, soil physics | 2,000+ |
| [groundSpring](https://github.com/syntheticChemistry/groundSpring) | Measurement noise, geochemistry, inverse problems | 930+ |
| [healthSpring](https://github.com/syntheticChemistry/healthSpring) | PK/PD, microbiome, biosignal, toxicology | 840+ |
| [ludoSpring](https://github.com/syntheticChemistry/ludoSpring) | Game science, HCI, procedural generation | 1,692 |
| [primalSpring](https://github.com/syntheticChemistry/primalSpring) | Composition patterns, federation, deploy graphs | 1,200+ |

### Live products

- [**footPrint**](https://footprint.primals.eco) — Sovereign GIS platform for archaeological and ecological survey
- [**esotericWebb**](https://webb.primals.eco) — Cross-evolution CRPG composed from rhizoCrypt + loamSpine + sweetGrass

### Organizations

| Org | Purpose |
|-----|---------|
| **ecoPrimals** | Infrastructure — 15 primals + tooling |
| [syntheticChemistry](https://github.com/syntheticChemistry) | Science validation — 9 springs |
| [sporeGarden](https://github.com/sporeGarden) | Deployable products and infrastructure compositions |
| [protoKarya](https://github.com/protoKarya) | User-facing applications for the wider world |

### How it's built

Every commit is AI-assisted ([K-NOME methodology](https://sporeprint.primals.eco/methodology/k-nome-programming/)) —
human constraint + AI implementation. `Co-authored-by: Cursor` on every commit.
11,000+ contributions in the last year from a single developer.

All code is `#![forbid(unsafe_code)]`. All primals cross-compile to 4 architectures
(x86_64 Linux, aarch64 Linux, aarch64 Android, x86_64 Windows).
59 statically-linked musl binaries in the depot.

### License

Code: [AGPL-3.0-or-later](https://www.gnu.org/licenses/agpl-3.0.html) &nbsp;|&nbsp;
Documents: [CC-BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/)

---

<sub>sporeprint.primals.eco — sovereign science, verifiable claims, no gatekeepers</sub>
