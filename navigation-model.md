# ZeroJS Navigation Model — Spec Outline

## 1. Purpose & Scope
Defines the deterministic, hydration‑free navigation model for ZeroJS.  
Covers: request initiation → boundary invocation → courier emission → representational assembly → streaming → completion.

ZeroJS navigation is:
- server‑driven  
- deterministic  
- reversible  
- domain‑agnostic  
- hydration‑free  

---

## 2. Navigation Philosophy
ZeroJS rejects SPA‑style client routing and hydration.  
Navigation is treated as:
- a **boundary transition**, not a client‑side state mutation  
- a **representational reconstruction**, not a diff  
- a **streaming event**, not a bundle execution  

Navigation is always:
- fetch‑based  
- FormData‑based  
- boundary‑safe  
- reversible  

---

## 3. Navigation Laws

### 3.1 No Hydration
ZeroJS never reconstructs server state on the client.  
Navigation always triggers a fresh representational pipeline.

### 3.2 No Client Routing
No client‑side routers, no virtual navigation stacks, no SPA semantics.

### 3.3 Deterministic Transitions
Identical navigation inputs must produce identical representational outputs.

### 3.4 Boundary-First Execution
Navigation always enters the boundary layer before any representational assembly.

### 3.5 Reversibility
Navigation transitions must be invertible:
FormData → Boundary → Courier → Representational → HTML → Representational → Courier.

---

## 4. Navigation Entry Points
Defines how navigation is initiated.

### 4.1 Link Navigation
Standard `<a>` navigation triggers:
- GET request  
- boundary invocation  
- courier construction  
- representational assembly  
- streaming HTML  

### 4.2 Form Navigation
Form submission triggers:
- POST request  
- FormData normalization  
- boundary invocation  
- courier construction  
- representational assembly  
- streaming HTML  

### 4.3 Programmatic Navigation
Navigation triggered via:
- `fetch()`  
- `FormData`  
- `URLSearchParams`  

Must follow the same deterministic pipeline.

---

## 5. Request Normalization
Defines how navigation requests are normalized.

- normalize method (GET/POST)  
- normalize URL  
- normalize FormData  
- strip domain semantics  
- produce boundary‑safe request envelope  

---

## 6. Boundary Invocation
Defines how navigation enters the boundary layer.

- create boundary context  
- execute domain logic  
- produce semantic outputs  
- emit courier seeds  

Boundary logic must not:
- manipulate representational structures  
- encode UI semantics  
- leak domain logic into couriers  

---

## 7. Courier Emission
Defines how navigation produces representational carriers.

- courier seeds → couriers  
- couriers must be reversible  
- couriers must be domain‑agnostic  
- couriers must be structurally typed  

---

## 8. Representational Assembly
Defines how couriers become UI structures.

- assemble nodes  
- assemble fragments  
- assemble representational primitives  
- apply deterministic transformations  
- produce UI tree  

No domain logic allowed.

---

## 9. Slot Composition
Defines how UI trees become ordered slot sequences.

- stable ordering  
- deterministic merging  
- reversible composition  
- produce slot list  

---

## 10. Streaming Navigation
Defines how navigation emits streaming HTML.

- emit slots in deterministic order  
- no hydration markers  
- no JS bundles  
- no client‑side reconstruction  
- streaming must be reversible  

---

## 11. Navigation Completion
Defines how navigation terminates.

- close stream  
- destroy couriers  
- emit final boundary metadata  
- produce deterministic termination signal  

---

## 12. Error Geometry
Defines how navigation errors propagate.

### 12.1 Boundary Errors
Converted into fallback courier seeds.

### 12.2 Courier Errors
Converted into structural fallback primitives.

### 12.3 Representational Errors
Converted into fallback slots.

### 12.4 Streaming Errors
Pipeline terminates gracefully with reversible metadata.

---

## 13. Reversibility Guarantees
Defines the formal guarantees of navigation reversibility.

- navigation transitions must be invertible  
- HTML output must reconstruct representational state  
- representational state must reconstruct couriers  
- courier lineage must be preserved  

---

## 14. Glossary References
Links to glossary terms for consistency:
- navigation  
- boundary  
- courier  
- representational domain  
- slot  
- reversible transition  
- membrane  
