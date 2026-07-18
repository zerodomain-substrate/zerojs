# ZeroJS Courier Lifecycle — Spec Outline

## 1. Purpose & Scope
Defines the full lifecycle of a ZeroJS courier — the membrane object responsible for carrying representational state across the boundary layer.  
Covers: creation → mutation → emission → representational assembly → destruction → reversibility.

Couriers are domain‑agnostic, reversible, structurally typed carriers of representational intent.

---

## 2. Courier Model Overview
Couriers serve as the **membrane object** between:
- **Boundary Layer** — domain logic, semantic operations.
- **Representational Domain** — UI primitives, slots, HTML streaming.

Couriers:
- carry *structure*, not meaning  
- enforce deterministic transitions  
- preserve reversibility  
- prevent domain logic from leaking into UI logic  

---

## 3. Courier Laws
Defines the strict rules governing courier behavior.

### 3.1 Domain-Agnostic Law
Couriers cannot encode domain semantics.  
They carry representational structure only.

### 3.2 Reversibility Law
Every courier transformation must be invertible.  
Courier → Representational → HTML → Representational → Courier.

### 3.3 Determinism Law
Courier transitions must produce identical outputs for identical inputs.  
No global state, no nondeterministic ordering.

### 3.4 Boundary Isolation Law
Couriers may cross the boundary, but domain logic may not cross into representational structures.

---

## 4. Courier Structure
Defines the structural components of a courier.

### 4.1 Courier Seed
Minimal structural output emitted by boundary logic.  
Contains only the information required to construct a courier.

### 4.2 Courier Body
Fully constructed courier containing:
- structural fields  
- representational metadata  
- reversible identifiers  
- typed primitives  

### 4.3 Courier Metadata
Metadata required for deterministic transitions:
- courierId  
- requestId  
- structural lineage  
- reversible markers  

---

## 5. Courier Lifecycle Stages

### 5.1 Creation
Boundary logic emits **courier seeds**.  
Membrane constructs full couriers from seeds.

Rules:
- creation must be deterministic  
- seeds must be domain‑agnostic  
- construction must be reversible  

---

### 5.2 Mutation
Couriers may undergo structural transformations.

Allowed mutations:
- structural refinement  
- representational augmentation  
- reversible transformations  

Forbidden mutations:
- semantic enrichment  
- domain logic injection  
- irreversible changes  

---

### 5.3 Emission
Couriers are emitted into the representational domain.

Emission rules:
- emission must be deterministic  
- emission order must be stable  
- couriers must remain domain‑agnostic  

---

### 5.4 Representational Assembly
Couriers are transformed into representational primitives:
- nodes  
- fragments  
- slots  

Assembly rules:
- transformations must be reversible  
- representational primitives must preserve courier structure  
- no domain logic allowed  

---

### 5.5 Slot Composition
Representational primitives are composed into deterministic slot sequences.

Slot rules:
- stable ordering  
- deterministic merging  
- reversible composition  

---

### 5.6 HTML Streaming
Slots are emitted as streaming HTML.

Streaming rules:
- no hydration markers  
- no client‑side reconstruction  
- reversible HTML emission  

---

### 5.7 Destruction
Couriers are destroyed after streaming completion.

Destruction rules:
- couriers cannot persist across requests  
- destruction must be deterministic  
- destruction must preserve reversibility metadata  

---

## 6. Error Lifecycle
Defines how errors propagate through courier transitions.

### 6.1 Boundary Errors
Converted into fallback courier seeds.

### 6.2 Courier Errors
Converted into structural fallback primitives.

### 6.3 Representational Errors
Converted into fallback slots.

### 6.4 Streaming Errors
Pipeline terminates gracefully with reversible metadata.

---

## 7. Reversibility Guarantees
Defines the formal guarantees of courier reversibility.

- courier → representational → HTML is invertible  
- HTML output can reconstruct representational state  
- representational state can reconstruct couriers  
- courier lineage must be preserved across transitions  

---

## 8. Deterministic Ordering Guarantees
Defines how courier transitions preserve ordering.

- courier emission order must be stable  
- representational assembly must be deterministic  
- slot composition must follow structural rules  
- streaming must follow slot order exactly  

---

## 9. Glossary References
Links to glossary terms for consistency:
- courier  
- courier seed  
- boundary  
- representational domain  
- reversible transition  
- slot  
- membrane  
