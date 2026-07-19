# ZeroJS Slot Model Specification

## 1. Purpose & Scope
The slot model defines the **ordered representational regions** used by ZeroJS to assemble and stream HTML.  
Slots are the final representational units before emission.  
They guarantee:
- deterministic ordering  
- reversible composition  
- domain‑agnostic structure  
- stable rendering semantics  

Slots are not components, templates, or DOM nodes.  
They are **representational containers**.

---

## 2. Slot Philosophy
ZeroJS treats slots as **structural boundaries** within the representational domain.  
They exist to ensure predictable rendering without hydration or client‑side routing.

Slots must:
- preserve representational ordering  
- remain domain‑agnostic  
- be fully reversible  
- encode structure, not semantics  
- serve as stable assembly targets  

Slots are the substrate’s “rendering zero.”

---

## 3. Slot Laws

### 3.1 Domain-Agnostic Law
Slots cannot encode domain semantics.  
They carry representational structure only.

### 3.2 Determinism Law
Identical representational graphs must produce identical slot sequences.

### 3.3 Reversibility Law
Slot composition must preserve enough structure to reconstruct representational primitives.

### 3.4 Isolation Law
Slots cannot contain domain logic, side effects, or client‑side state.

### 3.5 Stable Emission Law
Slot emission order must match slot composition order exactly.

---

## 4. Slot Structure

### 4.1 Slot Name
A stable identifier representing a UI region:
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
- fragments  
- structural markers  

Content must be domain‑agnostic.

### 4.3 Slot Metadata
Metadata required for deterministic assembly:
- `slotId`  
- courier lineage  
- structural ordering markers  
- reversible identifiers  

Metadata must not encode domain semantics.

---

## 5. Slot Lifecycle

### 5.1 Creation
Slots are created during representational assembly.  
Representational primitives → grouped by slot name → become slots.

### 5.2 Mutation
Slots may undergo reversible structural refinement:
- merging  
- splitting  
- augmentation  

All mutations must preserve ordering and lineage.

### 5.3 Composition
Slots are composed into a deterministic sequence:
- stable ordering  
- reversible grouping  
- domain‑agnostic structure  

### 5.4 Emission
Slots are emitted into the streaming pipeline.  
Emission order must match composition order exactly.

### 5.5 Destruction
Slots are destroyed after streaming completion.  
No slot may persist across requests.

---

## 6. Slot Ordering Rules

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

### 8.1 Deterministic Emission
Slots are emitted in stable order.

### 8.2 Reversible HTML
HTML must preserve enough structure to reconstruct slot boundaries.

### 8.3 No Hydration Markers
Slots cannot emit hydration metadata or client‑side reconstruction hints.

### 8.4 Structural Integrity
HTML must reflect slot boundaries clearly enough for reversible parsing.

---

## 9. Slot Error Geometry

### 9.1 Slot Creation Errors
Converted into fallback slots.

### 9.2 Slot Merge Errors
Converted into deterministic fallback ordering.

### 9.3 Streaming Errors
Slot lineage preserved for reversible termination.

### 9.4 Error Propagation
Errors propagate downstream as structural events.

---

## 10. Reversibility Guarantees

### 10.1 Representational Reconstruction
Slot boundaries must reconstruct representational primitives.

### 10.2 Courier Reconstruction
Representational primitives must reconstruct courier structure.

### 10.3 HTML Reconstruction
HTML must reconstruct slot boundaries and ordering.

Reversibility is a substrate invariant.

---

## 11. Slot Model Integration
The slot model integrates with:

- **representational domain** (upstream)  
- **rendering pipeline** (downstream)  
- **courier model** (indirect)  
- **membrane geometry** (transition)  
- **error geometry** (fallback)  
- **reversibility** (global invariant)  

Slots are the substrate’s final representational layer.

---

## 12. Glossary References
- slot  
- representational primitive  
- fragment  
- node  
- reversible transition  
- courier  
- streaming  
