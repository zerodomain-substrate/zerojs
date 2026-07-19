# ZeroJS Courier Model Specification

## 1. Purpose & Scope
The courier model defines the **membrane object** that carries structural, reversible, domain‑agnostic data from the boundary layer into the representational domain.

Couriers are the **first representational entities** in the ZeroJS pipeline.  
They are constructed from boundary‑emitted courier seeds and serve as the upstream input to representational assembly.

The courier model ensures:
- reversible membrane transitions  
- deterministic structural typing  
- domain‑agnostic representation  
- stable lineage propagation  
- safe upstream → downstream data flow  

Couriers are not components, templates, or UI constructs.  
They are **pure representational carriers**.

---

## 2. Courier Philosophy
Couriers are the **membrane’s structural objects**.  
They exist to isolate domain logic from representational logic.

A courier must:
- contain no domain semantics  
- preserve reversible lineage  
- encode structure deterministically  
- remain stable across membrane transitions  
- serve as the sole input to representational assembly  

Couriers are the substrate’s “representational zero.”

---

## 3. Courier Laws

### 3.1 Domain-Agnostic Law
Couriers cannot contain domain semantics.  
All domain meaning must be stripped during seed construction.

### 3.2 Determinism Law
Identical courier seeds must produce identical couriers.

### 3.3 Reversibility Law
Courier construction must preserve enough structure to reconstruct boundary outputs.

### 3.4 Structural Purity Law
Couriers must contain only:
- structural fields  
- lineage metadata  
- reversible identifiers  

### 3.5 Membrane Integrity Law
Couriers must not leak boundary logic into the representational domain.

---

## 4. Courier Structure

### 4.1 Courier Identity
Each courier must contain:
- `courierId` — reversible identifier  
- `lineage` — ancestry metadata  
- `requestId` — envelope lineage marker  

Identity must be deterministic and reversible.

### 4.2 Structural Payload
The payload contains:
- normalized structural data  
- membrane‑safe fields  
- domain‑agnostic values  

Payload must be free of:
- domain logic  
- representational primitives  
- UI semantics  

### 4.3 Courier Metadata
Metadata required for reversible transitions:
- boundaryId  
- membrane markers  
- structural ordering markers  

Metadata must not encode domain meaning.

---

## 5. Courier Lifecycle

### 5.1 Seed Construction (Boundary Layer)
Boundary logic emits **courier seeds**, which contain:
- domain results encoded structurally  
- reversible lineage markers  
- membrane‑safe data  

Seeds must be deterministic and domain‑agnostic.

### 5.2 Membrane Construction
Courier seeds cross the membrane and become full couriers:
- attach courierId  
- normalize payload  
- attach reversible metadata  
- strip domain semantics  

### 5.3 Courier Mutation
Couriers may undergo structural mutation:
- merging  
- splitting  
- augmentation  

All mutations must be reversible and deterministic.

### 5.4 Representational Emission
Couriers emit representational seeds:
- node seeds  
- fragment seeds  
- text seeds  

These seeds enter representational assembly.

### 5.5 Destruction
Couriers are destroyed after representational assembly.  
No courier may persist across requests.

---

## 6. Courier Operators

### 6.1 `constructCourier(seed)`
Constructs a full courier from a boundary-emitted seed.

### 6.2 `normalizeCourier(courier)`
Ensures deterministic shape and reversible metadata.

### 6.3 `mergeCouriers(a, b)`
Combines couriers into a single reversible courier.

### 6.4 `splitCourier(courier)`
Splits a courier into multiple reversible couriers.

### 6.5 `emitRepresentational(courier)`
Produces representational seeds for assembly.

All operators must be reversible and domain‑agnostic.

---

## 7. Deterministic Ordering Rules

### 7.1 Lineage Ordering
Courier lineage must preserve:
- boundary ordering  
- envelope ordering  
- membrane ordering  

### 7.2 Structural Ordering
Courier payload ordering must be deterministic.

### 7.3 Merge Ordering
Merged couriers must follow stable ordering rules.

### 7.4 Emission Ordering
Representational seeds must be emitted in deterministic order.

---

## 8. Courier Error Geometry

### 8.1 Courier Errors
Errors during courier construction or mutation must be converted into:
- fallback couriers  
- reversible error metadata  

### 8.2 Error Normalization
Courier errors must be:
- deterministic  
- domain‑agnostic  
- reversible  

### 8.3 Error Propagation
Errors propagate downstream as structural events.

---

## 9. Reversibility Guarantees

### 9.1 Boundary Reconstruction
Courier lineage must reconstruct boundary outputs.

### 9.2 Representational Reconstruction
Representational primitives must reconstruct courier structure.

### 9.3 Error Reconstruction
Fallback couriers must reconstruct error states.

Couriers are the reversible bridge between boundary and representational domain.

---

## 10. Courier Integration
Couriers integrate with:

- **boundary layer** (upstream)  
- **membrane geometry** (transition)  
- **representational assembly** (downstream)  
- **slot model** (indirect)  
- **reversibility** (global invariant)  
- **error geometry** (fallback)  

Couriers are the membrane’s structural backbone.

---

## 11. Glossary References
- courier  
- courier seed  
- membrane  
- lineage  
- representational seed  
- reversible transition  
- boundary  
