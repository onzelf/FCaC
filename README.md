# ✨ FCaC — Federated Computing as Code

FCaC is a **governance and admission substrate** for federated computation: it compiles explicit constraints into **verifiable boundary artifacts** and produces **auditable evidence** of admission and use.

---

## Manifesto 📣

### 1) Thesis
Federated systems fail in practice not because we cannot run distributed compute, but because we cannot **enforce and prove governance decisions at runtime across organizational boundaries**.

FCaC turns governance from documentation into **deterministic boundary enforcement**.

### 2) The Gap 🚧
Most federated platforms implicitly assume that admission control has been “solved” elsewhere (onboarding, IAM/RBAC configuration, post hoc logs). That works until:

- federations and stacks change (vendor/tool churn),
- operations expand beyond “train” (inference, evaluation, export, dataset-scoped actions),
- audits require *decision evidence* (“why allowed/denied, under which constraint, at that moment”).

**FCaC**’s claim is simple: **authorization must travel with the request as verifiable evidence**, not remain trapped in platform metadata.

### 3) The Primitive
FCaC centers on a boundary model:

**Policy/constraints → Admission artifact → Request-path verification → Decision record**

Concretely:
- constraints are compiled into a **capability admission artifact** (e.g., JWT)
- requests are bound to **proof-of-possession** (e.g., DPoP) to prove the requester holds the key **at request time**,
- the verifier enforces deterministically at the boundary and emits **structured decision evidence**.

### 4) ✅ What FCaC and the FC zoo are
- **FL**: one federated service (model training) among others.
- **FC**: the execution plane for federated workloads (training, inference, analytics, ETL) where assets remain local.
- **FCaC**: a separate governance/admission substrate that deterministically enforces constraints at boundaries and produces evidence.

### 5) ❌ What FCaC is not
FCaC is **not**:
- a new FL algorithm,
- a replacement for orchestration platforms,
- a privacy technique (DP/HE/SMPC), though it composes with them,
- “just tokens” or “just IAM”.

FCaC is about the missing link between **rules** and **requests**, **intent** and **design**

---

## 📜 An FCaC story (metaphor)

> The following metaphor clarifies the differences between FL vs FC vs FCaC.

An engineer arrives at a border to do a job. The engineer shows a **passport** (identity; identity alone is not permission) and a **work permit (JWT)** (what is allowed). The **border officer (gatekeeper)** verifies the permit deterministically and records **admission evidence**.

Inside, they use the country’s **infrastructure (FC)** to work where assets live. At the worksite, a **live badge challenge (DPoP)** proves the requester is the legitimate holder **at request time**. The job itself might be **FL training**, but that is just one permitted workload; real deployments require distinct rights for **training, inference, evaluation, export, and governed byproducts**.

**Without FCaC:** it becomes *illegal immigration* in the strict security sense—**entry and work occur without an enforceable admission gate and without evidence**—so bypass and accountability failure become the default.

**Without FC:** you may have border control, but no country to work in. Collaboration collapses back to centralization (move data, move compute, or move control), breaking sovereignty and local responsibility.

**With only FL:** collaborative training inside a presumed trust domain; cross-jurisdiction custody and differential rights over byproducts are not enforced at boundaries. Joining training implicitly grants ambiguous rights over the byproducts, and post-training custody/access becomes an out-of-band operational matter rather than a boundary-enforced, auditable regime.

---

## 🤕Three *failure* postcards (why FCaC exists)

1) **Audit day**  
A regulator (or internal risk) asks: *“Why was this operation allowed, under which rule, at that moment, and who had stop authority?”*   If the answer is “check the platform config and logs,” you do not have governance — you have reconstruction.

2) **Consortium drift**  
Partners, vendors, and toolchains change. RBAC settings, policies, and onboarding spreadsheets do not compose across stacks.   If authorization semantics don’t travel, the federation degrades into ad-hoc trust.

3) **Byproducts**  
Training is not the end. Models, metrics, embeddings, and predictions become governed assets.  
If “member-of-consortium” implicitly grants access to byproducts, you have a silent breach channel.

---

## BUT “platform IAM/RBAC + logs already solve admission,” 🤔

 - ***Platform IAM/RBAC*** and logs are necessary but ***do not fully address cross-silo session admission***. In multi-organization FL deployments, authorization decisions must be portable across
   administrative domains and justifiable from boundary-visible artifacts after execution.  
- Platform IAM typically governs local identities and resources, whereas our approach externalizes
   session-scoped authorization into request-carried capabilities bound to a holder key, enabling stateless verification and reproducible decision evidence at the session boundary. 
- The intent is therefore complementary: to make admission decisions explicit, portable, and
   auditable across organizational boundaries rather than embedded in platform configuration.

---

## First canonical disclosure and attribution ⚖️
- First public release: **[v0.9 (2025-11-07)](https://github.com/onzelf/FCaC/tree/v0.9), commit 44b3da0**
- SHA-256 of `README.md` at v0.9: **da95d644730a71c6b200992195d1c27a2d801aef2414a96d2e37fc4ced846962**

---

## 🛠️Technical repositories (start here if you want proof, not prose)
- [FCaC-MNIST (PoC / engineering docs)](https://github.com/onzelf/FCaC-MNIST)
- [FCaC-FLICS (PoC / engineering docs)](https://github.com/onzelf/FLICS-cross-silo-admission)
---


<div  align="center">

**Built with 🪄 for demonstrating Federated Computing as Code**

</div>

 
