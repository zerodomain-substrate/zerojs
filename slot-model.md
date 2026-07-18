# ZeroJS Slot Model — Spec Outline

## 1. Purpose & Scope
Defines the structural and deterministic rules governing **slots** — the ordered representational regions that ZeroJS uses to assemble and stream UI output.

Slots are the final representational units before HTML streaming.  
They ensure:
- deterministic ordering  
- reversible composition  
- domain‑agnostic structure  
- stable rendering semantics  

---

## 2. Slot Philosophy
Slots are not components, templates, or DOM nodes.  
They are **representational containers** that hold structured UI fragments.

ZeroJS treats slots as:
- deterministic boundaries  
- reversible structural units  
- stable assembly targets  
- domain‑agnostic representational primitives  

Slots exist to guarantee predictable rendering without hydration or client‑side routing.

---

## 3. Slot Laws

### 3.1 Determinism Law
Slot ordering must be stable and reproducible.  
Identical courier inputs must produce identical slot sequences.

### 3.2 Reversibility Law
Slot composition must be invertible:
Courier → Representational → Slot → HTML → Slot → Representational → Courier.

### 3.3 Domain-Agnostic Law
Slots cannot encode domain semantics.  
They carry representational structure only.

### 3.4 Isolation Law
Slots cannot contain domain logic, side effects, or client‑side state.

---

## 4. Slot Structure
Defines the structural fields of a slot.

### 4.1 Slot Name
A stable identifier representing the region:
- `"header"`
- `"main"`
- `"footer"`
- `"sidebar"`
- `"body"`

Names must be deterministic and reversible.

### 4.2 Slot Content
Structured representational fragments:
- nodes  
- text blocks  
- HTML fragments  
- representational primitives  

Content must be domain‑agnostic.

### 4.3 Slot Metadata
Metadata required for deterministic assembly:
- slotId  
- courier lineage  
- structural ordering markers  

---

## 5. Slot Lifecycle

### 5.1 Creation
Slots are created during representational assembly.  
Couriers emit representational primitives → primitives become slots.

### 5.2 Mutation
Slots may undergo structural refinement:
- merging  
- splitting  
- augmentation  

All mutations must be reversible.

### 5.3 Composition
Slots are composed into a deterministic sequence.  
Composition rules guarantee stable ordering.

### 5.4 Emission
Slots are emitted into the streaming pipeline.  
Emission order must match composition order exactly.

### 5.5 Destruction
Slots are destroyed after streaming completion.  
No slot may persist across requests.

---

## 6. Slot Ordering Rules
Defines how slot sequences maintain deterministic ordering.

### 6.1 Structural Ordering
Slots must follow structural rules defined by the representational domain.

### 6.2 Courier Lineage Ordering
Slots inherit ordering constraints from courier lineage.

### 6.3 Stable Merge Rules
When multiple couriers contribute to the same slot:
- merge deterministically  
- preserve reversibility  
- avoid nondeterministic interleaving  

### 6.4 Reversible Ordering
Slot order must be reconstructible from HTML output.

---

## 7. Slot Composition Model
Defines how slots are assembled into a final sequence.

### 7.1 Composition Operators
- `composeSlots(slots[])`  
- `mergeSlots(a, b)`  
- `splitSlot(slot)`  

All operators must be reversible.

### 7.2 Composition Phases
1. collect representational primitives  
2. group primitives by slot name  
3. merge groups deterministically  
4. produce final ordered slot list  

### 7.3 Composition Constraints
- no domain logic  
- no nondeterministic ordering  
- no irreversible transformations  

---

## 8. Slot → HTML Mapping
Defines how slots become streaming HTML.

### 8.1 Deterministic Emission
Slots are emitted in stable order.

### 8.2 Reversible HTML
HTML must preserve enough structure to reconstruct slots.

### 8.3 No Hydration Markers
Slots cannot emit hydration metadata or client‑side reconstruction hints.

---

## 9. Error Geometry

### 9.1 Slot Creation Errors
Converted into fallback slots.

### 9.2 Slot Merge Errors
Converted into deterministic fallback ordering.

### 9.3 Streaming Errors
Slot lineage preserved for reversible termination.

---

## 10. Reversibility Guarantees
Defines the formal guarantees of slot reversibility.

- slot composition must be invertible  
- HTML output must reconstruct slot boundaries  
- slot lineage must survive representational transitions  
- slot ordering must be reproducible  

---

## 11. Glossary References
Links to glossary terms for consistency:
- slot  
- courier  
- representational domain  
- boundary  
- reversible transition  
- membrane  
