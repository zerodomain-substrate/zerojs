# ZeroJS Error Geometry — Spec Outline

## 1. Purpose & Scope
Defines the structural, reversible, and deterministic handling of errors across the entire ZeroJS substrate.  
Error geometry ensures that failures:
- remain domain‑agnostic  
- preserve reversibility  
- maintain deterministic ordering  
- propagate safely across boundary → courier → representational → slot → streaming  

ZeroJS treats errors as **structural events**, not exceptional control flow.

---

## 2. Error Philosophy
ZeroJS rejects traditional exception semantics.  
Errors are treated as:
- representational states  
- reversible transitions  
- deterministic structural deviations  
- boundary‑safe membrane events  

Errors must never:
- leak domain logic  
- break reversibility  
- introduce nondeterminism  
- contaminate representational primitives  

---

## 3. Error Laws

### 3.1 Domain-Agnostic Law
Errors cannot encode domain semantics.  
They must be structural and representational only.

### 3.2 Reversibility Law
Error transitions must be invertible:
Error → Fallback Courier → Fallback Representational → Fallback Slot → HTML → Slot → Representational → Courier.

### 3.3 Determinism Law
Identical failing inputs must produce identical error outputs.

### 3.4 Isolation Law
Errors cannot cross the membrane with domain logic attached.

### 3.5 Non-Destructive Law
Errors must not destroy representational lineage or courier structure.

---

## 4. Error Types
Defines the structural categories of ZeroJS errors.

### 4.1 Boundary Errors
Errors originating from domain logic:
- invalid envelope  
- domain failure  
- semantic violation  

Converted into **fallback courier seeds**.

### 4.2 Courier Errors
Errors during courier construction or mutation:
- invalid courier seed  
- irreversible mutation  
- structural violation  

Converted into **fallback representational primitives**.

### 4.3 Representational Errors
Errors during representational assembly:
- invalid node  
- invalid fragment  
- ordering violation  

Converted into **fallback slots**.

### 4.4 Slot Errors
Errors during slot composition:
- merge failure  
- ordering conflict  
- reversible violation  

Converted into **fallback slot ordering**.

### 4.5 Streaming Errors
Errors during HTML emission:
- stream interruption  
- write failure  
- reversible termination  

Converted into **graceful termination signals**.

---

## 5. Error Lifecycle

### 5.1 Detection
Errors detected at:
- boundary invocation  
- courier construction  
- representational assembly  
- slot composition  
- streaming emission  

Detection must be deterministic.

### 5.2 Normalization
Errors normalized into structural error objects:
- errorId  
- errorType  
- reversible metadata  
- courier lineage  

### 5.3 Fallback Construction
Fallback structures must be:
- reversible  
- deterministic  
- domain‑agnostic  

### 5.4 Propagation
Errors propagate across layers without:
- semantic enrichment  
- nondeterministic branching  
- irreversible transitions  

### 5.5 Termination
Streaming errors produce:
- reversible termination metadata  
- deterministic closure  

---

## 6. Error Operators

### 6.1 `normalizeError(rawError)`
Converts raw errors into structural error objects.

### 6.2 `fallbackCourier(error)`
Constructs reversible fallback couriers.

### 6.3 `fallbackRepresentational(error)`
Constructs fallback representational primitives.

### 6.4 `fallbackSlots(error)`
Constructs fallback slot sequences.

### 6.5 `terminateStream(error)`
Gracefully terminates streaming with reversible metadata.

All operators must be reversible.

---

## 7. Deterministic Ordering Rules

### 7.1 Error Ordering
Errors must preserve:
- courier lineage  
- representational ordering  
- slot ordering  

### 7.2 Fallback Ordering
Fallback structures must follow deterministic ordering rules.

### 7.3 Streaming Ordering
Streaming must preserve slot order even during fallback.

---

## 8. Reversibility Guarantees
Defines the formal guarantees of error reversibility.

- error transitions must be invertible  
- fallback couriers must reconstruct original lineage  
- fallback representational primitives must reconstruct courier structure  
- fallback slots must reconstruct representational ordering  
- HTML output must reconstruct error lineage  

---

## 9. Error Geometry Diagrams
References to diagrams (optional):
- error propagation graph  
- reversible fallback flow  
- membrane error transitions  

---

## 10. Glossary References
Links to glossary terms for consistency:
- error geometry  
- boundary  
- courier  
- representational domain  
- slot  
- reversible transition  
- membrane  
