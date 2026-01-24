# FCaC — Federated Computing as Code

FCaC is a governance and admission substrate for federated computation: it compiles explicit constraints into verifiable boundary artifacts and produces auditable evidence of admission and use.

## Definitions
- **FL**: one federated service (model training) among others.
- **FC**: the execution plane for federated workloads (training, inference, analytics, ETL) where assets remain local.
- **FCaC**: a separate governance/admission substrate that deterministically enforces constraints at boundaries and produces evidence.

## An FCaC story
An engineer arrives at a border to do a job.

They show a **passport** (identity) and a **work permit (ECT)** (what is allowed). The **border officer (the gatekeeper)** verifies the permit deterministically and records **evidence**. Inside, they use the country’s **infrastructure (FC)** to work where assets live. At the worksite, a **live badge challenge (DPoP)** proves the requester is the legitimate holder now. The job itself might be **FL training**, but that is just one permitted workload; byproducts are governed assets with capability-scoped access.

**Without FCaC:** illegal immigration—work happens without deterministic admission or an evidence trail; infiltration and accountability failure become the default.  
**Without FC:** border control exists, but no place to work—collaboration collapses to centralization (move data/compute/control).  
**With only FL:** collaborative training inside a presumed trust domain; cross-jurisdiction custody and differential rights over byproducts are not enforced at boundaries.

## Provenance (canonical disclosure)
- First public release: **v0.9 (2025-11-07), commit 44b3da0**
- SHA-256 of `README.md` at v0.9:
  **da95d644730a71c6b200992195d1c27a2d801aef2414a96d2e37fc4ced846962**

## Technical repositories
- [FCaC-MNIST (PoC / engineering doxs)](https://github.com/onzelf/FCaC-MNIST)
- [FCaC-FLICS (PoC / engineering docs)](https://github.com/onzelf/FCaC-FLICS)
