# ZeroJS Representational Assembly — Spec Outline

## 1. Purpose & Scope
Defines how couriers are transformed into **representational primitives** — the structural UI units used by ZeroJS before slot composition and HTML streaming.

Representational assembly ensures:
- deterministic UI structure  
- reversible transformations  
- domain‑agnostic representation  
- stable rendering semantics  

---

## 2. Assembly Philosophy
ZeroJS treats UI as a **representational graph**, not a component tree.

Representational assembly:
- converts courier structure → representational primitives  
- enforces deterministic ordering  
- preserves reversibility  
- avoids domain logic entirely  
- produces a stable UI tree for slot composition  

Representational primitives are the “atoms” of ZeroJS UI.

---

## 3. Assembly Laws

### 3.1 Domain-Agnostic Law
Representational primitives cannot encode domain semantics.  
They carry structure only.

### 3.2 Determinism Law
Identical courier inputs must produce identical representational graphs.

### 3.3 Reversibility Law
Assembly must be invertible:
Courier → Representational → Slot → HTML → Slot → Representational → Courier.

### 3.4 Isolation Law
Representational assembly cannot invoke domain logic or mutate boundary state.

---

## 4. Representational Primitives
Defines the structural units produced during assembly.

### 4.1 Node
A structural UI element:
- tag  
- attributes  
- children  
- metadata  

### 4.2 Fragment
A grouping of nodes:
- preserves ordering  
- reversible  
- domain‑agnostic  

### 4.3 Text Block
A typed text primitive:
- raw text  
- reversible encoding  
- deterministic placement  

### 4.4 Structural Marker
Metadata required for deterministic assembly:
- courier lineage  
- structural ordering markers  
- reversible identifiers  

---

## 5. Assembly Lifecycle

### 5.1 Collection
Couriers emit representational seeds:
- node seeds  
- fragment seeds  
- text seeds  

Seeds must be domain‑agnostic.

### 5.2 Construction
Seeds become full representational primitives:
- construct nodes  
- construct fragments  
- construct text blocks  

Construction must be reversible.

### 5.3 Refinement
Primitives may undergo structural refinement:
- merging  
- splitting  
- augmentation  

Refinement must preserve reversibility.

### 5.4 Graph Assembly
Primitives are assembled into a deterministic UI graph:
- stable ordering  
- deterministic grouping  
- reversible structure  

### 5.5 Slot Preparation
UI graph is prepared for slot composition:
- group by slot name  
- preserve ordering  
- attach reversible metadata  

---

## 6. Deterministic Ordering Rules

### 6.1 Structural Ordering
Nodes must follow structural rules defined by the representational domain.

### 6.2 Courier Lineage Ordering
Representational primitives inherit ordering constraints from courier lineage.

### 6.3 Stable Merge Rules
When multiple couriers contribute to the same region:
- merge deterministically  
- avoid nondeterministic interleaving  
- preserve reversible structure  

### 6.4 Reversible Ordering
Representational ordering must be reconstructible from HTML output.

---

## 7. Assembly Operators

### 7.1 `assembleNodes(courier)`
Constructs node primitives from courier structure.

### 7.2 `assembleFragments(nodes[])`
Groups nodes into reversible fragments.

### 7.3 `assembleTextBlocks(courier)`
Constructs typed text primitives.

### 7.4 `assembleGraph(primitives[])`
Builds the deterministic UI graph.

All operators must be reversible.

---

## 8. Representational → Slot Mapping
Defines how representational primitives become slots.

### 8.1 Grouping
Group primitives by slot name.

### 8.2 Merging
Merge groups deterministically.

### 8.3 Ordering
Produce a stable slot list.

### 8.4 Reversibility
Slot boundaries must preserve enough structure to reconstruct primitives.

---

## 9. Error Geometry

### 9.1 Assembly Errors
Converted into fallback representational primitives.

### 9.2 Merge Errors
Converted into deterministic fallback ordering.

### 9.3 Slot Preparation Errors
Converted into fallback slot groups.

### 9.4 Streaming Errors
Representational lineage preserved for reversible termination.

---

## 10. Reversibility Guarantees
Defines the formal guarantees of representational reversibility.

- representational assembly must be invertible  
- HTML output must reconstruct representational primitives  
- representational lineage must survive slot transitions  
- representational ordering must be reproducible  

---

## 11. Glossary References
Links to glossary terms for consistency:
- representational domain  
- courier  
- node  
- fragment  
- text block  
- slot  
- reversible transition  
- membrane  
