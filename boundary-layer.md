# ZeroJS Boundary Layer Specification

## 1. Purpose & Scope
The boundary layer is the **semantic zero** of ZeroJS — the upstream stratum where domain logic executes and where representational structure begins.  
It receives normalized request envelopes and emits **courier seeds**, which cross the membrane into the representational domain.

The boundary layer:
- executes domain logic  
- isolates domain semantics  
- emits reversible courier seeds  
- defines the upstream geometry of the membrane  
- anchors the entire reversible pipeline  

No representational logic may exist in the boundary layer.

---

## 2. Boundary Layer Philosophy
ZeroJS treats the boundary as the **only place where domain semantics may exist**.  
Everything downstream (couriers, representational primitives, slots, HTML) must be domain‑agnostic.

The boundary layer must:
- isolate domain logic  
- avoid representational constructs  
- emit purely structural courier seeds  
- preserve reversible lineage  
- remain deterministic  

The boundary is not a controller, router, or component system.  
It is a **semantic membrane source**.

---

## 3. Boundary Layer Laws

### 3.1 Domain Logic Containment
All domain semantics must remain inside the boundary.  
No domain meaning may cross the membrane.

### 3.2 Structural Output Law
Boundary outputs must be **courier seeds**, not representational primitives.

### 3.3 Determinism Law
Identical envelopes must produce identical boundary outputs.

### 3.4 Reversibility Law
Boundary outputs must preserve enough structure to reconstruct envelope lineage.

### 3.5 Membrane Integrity Law
Boundary → courier transitions must remain reversible and domain‑agnostic.

---

## 4. Boundary Inputs

### 4.1 Request Envelope
The boundary receives a normalized envelope containing:
- method  
- URL  
- FormData  
- structural metadata  

The envelope is the **only** input to the boundary layer.

### 4.2 Boundary Context
A deterministic context constructed from:
- envelope metadata  
- domain configuration  
- reversible lineage markers  

The context must not contain representational constructs.

---

## 5. Boundary Outputs

### 5.1 Courier Seeds
The boundary emits **courier seeds**, which are:
- minimal structural objects  
- domain‑agnostic  
- reversible  
- membrane‑safe  

Courier seeds contain:
- structural data  
- lineage metadata  
- domain results encoded structurally  

### 5.2 Boundary Metadata
Metadata required for reversible transitions:
- requestId  
- boundaryId  
- lineage markers  

Boundary metadata must not encode domain semantics.

---

## 6. Boundary Execution Model

### 6.1 Domain Logic Execution
Domain logic runs inside the boundary context.  
It may:
- read envelope data  
- perform domain operations  
- produce domain results  

It may not:
- construct representational primitives  
- manipulate slots  
- emit HTML  
- encode UI semantics  

### 6.2 Seed Construction
Domain results are converted into courier seeds via:
- structural normalization  
- reversible encoding  
- lineage preservation  

### 6.3 Membrane Preparation
Courier seeds are prepared for membrane transition:
- attach reversible metadata  
- strip domain semantics  
- ensure deterministic shape  

---

## 7. Boundary Error Geometry

### 7.1 Boundary Errors
Errors occurring inside the boundary must be converted into:
- fallback courier seeds  
- reversible error metadata  

### 7.2 Error Normalization
Boundary errors must be:
- deterministic  
- domain‑agnostic  
- reversible  

### 7.3 Error Propagation
Errors propagate downstream as structural events, not exceptions.

---

## 8. Boundary → Courier Transition

### 8.1 Membrane Crossing
Courier seeds cross the membrane and become full couriers.  
The membrane enforces:
- domain isolation  
- reversible transitions  
- deterministic construction  

### 8.2 Structural Guarantees
Courier construction must preserve:
- lineage  
- ordering  
- structural integrity  

### 8.3 Domain-Agnostic Guarantees
No domain semantics may remain in the courier.

---

## 9. Reversibility Guarantees

### 9.1 Envelope Reconstruction
Boundary metadata must allow reconstruction of envelope lineage.

### 9.2 Courier Reconstruction
Courier lineage must reconstruct boundary outputs.

### 9.3 Error Reconstruction
Fallback couriers must reconstruct boundary error states.

Reversibility begins at the boundary.

---

## 10. Boundary Layer Integration
The boundary layer integrates with:

- **request envelope** (upstream)  
- **courier model** (downstream)  
- **membrane geometry** (transition)  
- **error geometry** (fallback)  
- **reversibility** (global invariant)  

The boundary is the anchor of the entire substrate.

---

## 11. Glossary References
- boundary  
- envelope  
- courier seed  
- membrane  
- lineage  
- reversibility  
- domain logic  
