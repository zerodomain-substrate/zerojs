# ZeroJS Request Envelope — Spec Outline

## 1. Purpose & Scope
Defines the deterministic, boundary‑safe request envelope used by ZeroJS.  
The request envelope is the **canonical, normalized representation** of incoming navigation events (GET, POST, fetch, FormData).

It ensures:
- domain‑agnostic structure  
- reversible normalization  
- deterministic boundary invocation  
- stable courier construction  

---

## 2. Envelope Philosophy
ZeroJS treats requests as **structural inputs**, not semantic events.

The envelope:
- strips domain semantics  
- normalizes transport details  
- preserves only representationally relevant structure  
- guarantees deterministic reconstruction  

---

## 3. Envelope Laws

### 3.1 Domain-Agnostic Law
The envelope cannot encode domain meaning.  
It carries structure only.

### 3.2 Determinism Law
Identical raw requests must produce identical envelopes.

### 3.3 Reversibility Law
Envelope → Boundary → Courier → Representational → HTML must be invertible.

### 3.4 Boundary-Safe Law
Envelope must be safe to pass into the boundary layer without leaking transport semantics.

---

## 4. Envelope Structure
Defines the structural fields of the request envelope.

### 4.1 Method
Normalized HTTP method:
- `GET`
- `POST`

### 4.2 URL
Normalized URL:
- pathname  
- search params  
- canonical ordering of query keys  

### 4.3 FormData
Normalized form payload:
- stable key ordering  
- reversible value encoding  
- domain‑agnostic structure  

### 4.4 Metadata
Structural metadata:
- requestId  
- timestamp (optional, deterministic format)  
- navigation type (link, form, fetch)  

---

## 5. Normalization Rules
Defines how raw requests become envelopes.

### 5.1 Method Normalization
Convert method to uppercase.  
Reject unsupported methods.  
Guarantee deterministic method representation.

### 5.2 URL Normalization
- canonicalize pathname  
- sort query parameters  
- normalize encoding  
- strip domain semantics  

### 5.3 FormData Normalization
- stable key ordering  
- reversible encoding  
- deterministic flattening rules  
- no semantic enrichment  

### 5.4 Metadata Normalization
- generate requestId  
- classify navigation type  
- attach reversible metadata  

---

## 6. Envelope Lifecycle

### 6.1 Creation
Raw request → normalized envelope.  
Must be deterministic and reversible.

### 6.2 Boundary Invocation
Envelope enters the boundary layer.  
Boundary logic receives only envelope fields, never raw request objects.

### 6.3 Courier Seeding
Boundary logic emits courier seeds based on envelope structure.

### 6.4 Representational Assembly
Envelope influences representational assembly only through courier structure.

### 6.5 Destruction
Envelope is destroyed after pipeline completion.  
No envelope may persist across requests.

---

## 7. Error Geometry

### 7.1 Normalization Errors
Converted into deterministic error envelopes.

### 7.2 Boundary Errors
Envelope is preserved for reversible debugging.

### 7.3 Representational Errors
Envelope metadata is used for fallback rendering.

### 7.4 Streaming Errors
Envelope lineage is preserved for reversible termination.

---

## 8. Reversibility Guarantees
Defines the formal guarantees of envelope reversibility.

- raw request → envelope is invertible  
- envelope → courier is invertible  
- envelope metadata must survive representational transitions  
- HTML output must reconstruct envelope lineage  

---

## 9. Deterministic Ordering Guarantees
Defines how envelope normalization preserves ordering.

- query params sorted  
- FormData keys sorted  
- metadata fields stable  
- envelope construction reproducible  

---

## 10. Glossary References
Links to glossary terms for consistency:
- request envelope  
- boundary  
- courier  
- representational domain  
- reversible transition  
- slot  
- membrane  
