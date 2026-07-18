# ZeroJS Reversibility — Spec Outline

## 1. Purpose & Scope
Defines the reversible laws governing all ZeroJS substrate transitions.  
Reversibility ensures that every transformation across:
- boundary  
- courier  
- representational domain  
- slot model  
- streaming HTML  

…can be inverted without loss of structural information.

Reversibility is the **core invariant** of ZeroJS.

---

## 2. Reversibility Philosophy
ZeroJS treats UI rendering as a **reversible representational pipeline**, not a one‑way transformation.

Reversibility guarantees:
- structural integrity  
- deterministic reconstruction  
- domain‑agnostic transitions  
- stable lineage across layers  

Reversibility is required for:
- debugging  
- correctness  
- deterministic rendering  
- substrate purity  

---

## 3. Reversibility Laws

### 3.1 Structural Preservation Law
Every transformation must preserve enough structure to reconstruct its input.

### 3.2 Deterministic Inversion Law
Inversion must be deterministic:
Output → Input must produce identical results for identical inputs.

### 3.3 Domain-Agnostic Law
Reversibility cannot depend on domain semantics.  
Only structural information may be used.

### 3.4 Membrane Integrity Law
Cross‑boundary transitions must remain reversible without leaking domain logic.

### 3.5 Non-Destructive Law
No irreversible mutations are allowed at any stage.

---

## 4. Reversible Pipeline Overview
Defines the reversible mapping across all substrate layers.

### 4.1 Envelope → Boundary
Normalized request envelope must reconstruct raw request structure.

### 4.2 Boundary → Courier
Courier seeds must reconstruct boundary outputs.

### 4.3 Courier → Representational
Representational primitives must reconstruct courier structure.

### 4.4 Representational → Slot
Slot sequences must reconstruct representational ordering.

### 4.5 Slot → HTML
HTML output must reconstruct slot boundaries and ordering.

### 4.6 HTML → Representational (Reverse)
HTML must contain enough structure to reconstruct representational primitives.

### 4.7 Representational → Courier (Reverse)
Reconstructed primitives must reconstruct courier lineage.

---

## 5. Reversible Structures

### 5.1 Reversible Identifiers
All layers must include reversible identifiers:
- requestId  
- courierId  
- slotId  
- lineage markers  

### 5.2 Reversible Metadata
Metadata must be:
- structural  
- domain‑agnostic  
- invertible  

### 5.3 Reversible Ordering
Ordering must be:
- stable  
- deterministic  
- reconstructible  

---

## 6. Reversible Operators

### 6.1 `invertEnvelope(html)`
Reconstructs envelope lineage from HTML metadata.

### 6.2 `invertCourier(representational)`
Reconstructs courier structure from representational primitives.

### 6.3 `invertRepresentational(slots)`
Reconstructs representational graph from slot sequences.

### 6.4 `invertSlots(html)`
Reconstructs slot boundaries from HTML output.

All operators must be deterministic and domain‑agnostic.

---

## 7. Reversible Assembly Rules

### 7.1 Node Reversibility
Nodes must preserve:
- tag  
- attributes  
- children  
- ordering  

### 7.2 Fragment Reversibility
Fragments must preserve grouping and lineage.

### 7.3 Text Block Reversibility
Text blocks must preserve reversible encoding.

### 7.4 Slot Reversibility
Slots must preserve:
- boundaries  
- ordering  
- lineage markers  

---

## 8. Reversible Streaming Rules

### 8.1 Structural HTML
HTML must contain enough structure to reconstruct:
- slot boundaries  
- representational primitives  
- courier lineage  

### 8.2 No Hydration Markers
Hydration markers break reversibility and are forbidden.

### 8.3 Deterministic Emission
Streaming must follow deterministic slot order.

---

## 9. Error Reversibility

### 9.1 Error Lineage Preservation
Errors must preserve reversible lineage.

### 9.2 Fallback Reversibility
Fallback couriers, primitives, and slots must be invertible.

### 9.3 Termination Reversibility
Streaming termination must preserve reversible metadata.

---

## 10. Reversibility Guarantees
Formal guarantees:

- Every pipeline stage is invertible.  
- HTML output reconstructs representational state.  
- Representational state reconstructs couriers.  
- Couriers reconstruct boundary outputs.  
- Envelope lineage is preserved across all transitions.  
- Ordering is stable and reversible.  

Reversibility is a **substrate invariant**.

---

## 11. Glossary References
Links to glossary terms:
- reversibility  
- courier  
- representational domain  
- slot  
- boundary  
- membrane  
- lineage  
