# ZeroJS Root Specification

## 1. Purpose & Scope
ZeroJS is a **reversible, deterministic, domain‑agnostic rendering substrate**.  
It defines a complete representational pipeline from request → HTML, without hydration, client‑side routing, or component semantics.

This root specification establishes:
- the substrate identity  
- the substrate laws  
- the reversible pipeline  
- the four core layers  
- the membrane geometry  
- the global invariants  

All other ZeroJS specs refine the concepts defined here.

---

## 2. Substrate Identity
ZeroJS is not a framework.  
ZeroJS is a **substrate** — a representational foundation with strict structural laws.

A substrate:
- defines representational primitives  
- defines reversible transitions  
- defines membrane boundaries  
- defines deterministic ordering  
- defines domain‑agnostic structure  

ZeroJS is the substrate for reversible UI rendering.

---

## 3. Substrate Laws

### 3.1 Determinism Law
Identical inputs must produce identical outputs across all layers.

### 3.2 Reversibility Law
Every transformation must be invertible:
Envelope → Boundary → Courier → Representational → Slot → HTML → Slot → Representational → Courier.

### 3.3 Domain-Agnostic Law
Domain semantics must never leak into representational structures.

### 3.4 Membrane Integrity Law
Boundary transitions must remain isolated and reversible.

### 3.5 Non-Destructive Law
No irreversible mutations allowed anywhere in the pipeline.

These laws govern the entire substrate.

---

## 4. Core Layers
ZeroJS consists of four core layers, each defined in its own specification.

### 4.1 **Boundary Layer**  
The upstream semantic zone.  
Executes domain logic and emits courier seeds.  
Defines the substrate’s “semantic zero.”

### 4.2 **Courier Model**  
The membrane object.  
Carries reversible, domain‑agnostic structure into the representational domain.  
Defines the substrate’s “representational zero.”

### 4.3 **Representational Domain**  
Constructs representational primitives (nodes, fragments, text blocks).  
Assembles the reversible UI graph.  
Defines the substrate’s “UI zero.”

### 4.4 **Slot Model**  
Groups representational primitives into deterministic slot sequences.  
Defines the substrate’s “rendering zero.”

These four layers form the substrate’s structural backbone.

---

## 5. Full Reversible Pipeline
ZeroJS defines a reversible representational chain:

```
Envelope
   ↓
Boundary Layer
   ↓
Courier Model (Membrane)
   ↓
Representational Domain
   ↓
Slot Model
   ↓
Rendering Pipeline (Streaming HTML)
   ↓
Navigation Model
   ↓
Envelope (repeat)
```

Reversibility flows in the opposite direction.

---

## 6. Membrane Geometry
The membrane is the reversible boundary between:
- boundary layer  
- courier model  
- representational domain  

The membrane enforces:
- domain isolation  
- reversible transitions  
- deterministic construction  
- structural purity  

The membrane is the substrate’s structural join layer.

---

## 7. Representational Primitives
ZeroJS defines a minimal set of reversible primitives:

- nodes  
- fragments  
- text blocks  
- structural markers  

These primitives form the representational graph and feed into slot composition.

---

## 8. Ordering Guarantees
Ordering is part of reversibility.

ZeroJS guarantees:
- envelope ordering  
- courier lineage ordering  
- representational ordering  
- slot ordering  
- streaming ordering  

Ordering must be stable and reconstructible.

---

## 9. Error Geometry
Errors are structural events, not exceptions.

Error propagation:
- boundary error → fallback courier  
- courier error → fallback representational  
- representational error → fallback slot  
- streaming error → reversible termination  

Errors must preserve lineage and reversibility.

---

## 10. Substrate Cohesion Guarantees
ZeroJS behaves as one coherent representational machine.

Guarantees:
- all layers join cleanly  
- no nondeterminism  
- no domain leakage  
- no irreversible transitions  
- no hydration  
- no client‑side routing  

ZeroJS is a **pure representational substrate**.

---

## 11. Glossary References
- substrate  
- membrane  
- courier  
- representational domain  
- slot  
- lineage  
- reversibility  
- boundary  
