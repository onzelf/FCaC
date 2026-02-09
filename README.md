# FCaC — Federated Computing as Code

FCaC is a governance and admission substrate for federated computation: it compiles explicit constraints into verifiable boundary artifacts and produces auditable evidence of admission and use.

## Definitions
- **FL**: one federated service (model training) among others.
- **FC**: the execution plane for federated workloads (training, inference, analytics, ETL) where assets remain local.
- **FCaC**: a separate governance/admission substrate that deterministically enforces constraints at boundaries and produces evidence.

---

## An FCaC story
>The following metaphor can help to clarify the differences between FL vs FC vs FCaC.

An engineer arrives at a border to do a job.

The engineer shows a **passport** (identity) and a **work permit (ECT)** (what is allowed). The **border officer (gatekeeper)** verifies the permit deterministically and records **admission evidence**. Inside, they use the country’s **infrastructure (FC)** to work where assets live. At the worksite, a **live badge challenge (DPoP)** proves the requester is the legitimate holder **at request time**. The job itself might be **FL training**, but that is just one permitted workload; **byproducts are governed assets** with capability-scoped access.

**Without FCaC:** It is *illegal immigration*, you can cross and work, but without an enforceable admission regime—no proof-carrying authorization, no deterministic gate, no evidence trail—so infiltration risk and accountability failure become the default.

**Without FC:** You may have border control, but no country to work in. Collaboration collapses back to centralization (move data, move compute, or move control), breaking sovereignty and local responsibility.

**With only FL:** Collaborative training inside a presumed trust domain; cross-jurisdiction custody and differential rights over byproducts are not enforced at boundaries. Joining training implicitly grants ambiguous rights over the byproducts, and post-training custody/access becomes an out-of-band operational matter rather than a boundary-enforced, auditable regime.


## Provenance (canonical disclosure)
- First public release: **[v0.9 (2025-11-07)](https://github.com/onzelf/FCaC/tree/v0.9), commit 44b3da0**
- SHA-256 of `README.md` at v0.9:
  **da95d644730a71c6b200992195d1c27a2d801aef2414a96d2e37fc4ced846962**

## Technical repositories
- [FCaC-MNIST (PoC / engineering docs)](https://github.com/onzelf/FCaC-MNIST)
- [FCaC-FLICS (PoC / engineering docs)](https://github.com/onzelf/FLICS-cross-silo-admission)
