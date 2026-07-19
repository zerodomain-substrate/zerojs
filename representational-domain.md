# ZeroJS Representational Domain Specification

## 1. Purpose & Scope
The representational domain is the **structural UI space** where couriers become representational primitives.  
It is the first layer where UI structure exists, but it remains strictly **domain‑agnostic** and **reversible**.

The representational domain:
- receives couriers  
- constructs representational primitives  
- assembles the UI graph  
- prepares slot groups  
- preserves reversible lineage  
- guarantees deterministic ordering  

No domain logic may exist in the representational domain.

---

## 2. Representational Philosophy
ZeroJS treats UI as a **reversible representational graph**, not a component tree.

The representational domain must:
- encode structure, not semantics  
- preserve ordering deterministically  
- remain fully reversible  
- avoid domain logic  
- prepare primitives for slot composition  

Representational primitives are the substrate’s “UI atoms.”

---

## 3. Representational Laws

### 3.1 Domain-Agnostic Law
Representational primitives cannot encode domain semantics.  
They carry structure only.

### 3.2 Determinism Law
Identical couriers must produce identical representational graphs.

### 3.3 Reversibility Law
Representational assembly must preserve enough structure to reconstruct courier lineage.

### 3.4 Structural Purity Law
Representational primitives must contain only:
- tags  
- attributes  
- children  
- text  
- structural markers  
- lineage metadata  

### 3.5 Non-Destructive Law
Representational assembly must not mutate or destroy courier structure.

---

## 4. Representational Primitives

### 4.1 Node
A structural UI element containing:
- tag  
- attributes  
- children  
- lineage metadata  

Nodes must be reversible and domain‑agnostic.

### 4.2 Fragment
A reversible grouping of nodes:
- preserves ordering  
- contains no domain semantics  
- acts as a structural container  

Fragments must not introduce new semantics.

### 4.3 Text Block
A typed text primitive containing:
- raw text  
- reversible encoding  
- deterministic placement  

Text blocks must not encode domain meaning.

### 4.4 Structural Marker
Metadata required for deterministic assembly:
- ordering markers  
- lineage markers  
- reversible identifiers  

Markers must not encode domain semantics.

---

## 5. Representational Assembly

### 5.1 Seed Collection
Couriers emit representational seeds:
- node seeds  
- fragment seeds  
- text seeds  

Seeds must be domain‑agnostic.

### 5.2 Primitive Construction
Seeds become full representational primitives:
- construct nodes  
- construct fragments  
- construct text blocks  

Construction must be deterministic and reversible.

### 5.3 Structural Refinement
Primitives may undergo reversible refinement:
- merging  
- splitting  
- augmentation  

Refinement must preserve ordering and lineage.

### 5.4 UI Graph Assembly
Primitives are assembled into a deterministic UI graph:
- stable ordering  
- reversible structure  
- domain‑agnostic grouping  

### 5.5 Slot Preparation
UI graph is prepared for slot composition:
- group primitives by slot name  
- attach reversible metadata  
- preserve ordering  

---

## 6. Deterministic Ordering Rules

### 6.1 Courier Lineage Ordering
Representational primitives must inherit ordering from courier lineage.

### 6.2 Structural Ordering
Nodes must follow structural rules defined by the representational domain.

### 6.3 Merge Ordering
Merged primitives must follow deterministic ordering rules.

### 6.4 Graph Ordering
UI graph ordering must be reconstructible from HTML output.

---

## 7. Representational Operators

### 7.1 `assembleNodes(courier)`
Constructs node primitives from courier structure.

### 7.2 `assembleFragments(nodes[])`
Groups nodes into reversible fragments.

### 7.3 `assembleTextBlocks(courier)`
Constructs typed text primitives.

### 7.4 `assembleGraph(primitives[])`
Builds the deterministic UI graph.

### 7.5 `prepareSlots(graph)`
Groups primitives into slot sequences.

All operators must be reversible and domain‑agnostic.

---

## 8. Representational Error Geometry

### 8.1 Representational Errors
Errors during assembly must be converted into:
- fallback primitives  
- reversible error metadata  

### 8.2 Error Normalization
Representational errors must be:
- deterministic  
- domain‑agnostic  
- reversible  

### 8.3 Error Propagation
Errors propagate downstream as structural events.

---

## 9. Reversibility Guarantees

### 9.1 Courier Reconstruction
Representational primitives must reconstruct courier structure.

### 9.2 Slot Reconstruction
Slot boundaries must reconstruct representational ordering.

### 9.3 HTML Reconstruction
HTML must reconstruct representational primitives.

Reversibility is a substrate invariant.

---

## 10. Representational Domain Integration
The representational domain integrates with:

- **courier model** (upstream)  
- **slot model** (downstream)  
- **membrane geometry** (transition)  
- **rendering pipeline** (streaming)  
- **error geometry** (fallback)  
- **reversibility** (global invariant)  

The representational domain is the substrate’s structural UI layer.

---

## 11. Glossary References
- representational domain  
- node  
- fragment  
- text block  
- structural marker  
- courier  
- reversible transition  
- slot  
