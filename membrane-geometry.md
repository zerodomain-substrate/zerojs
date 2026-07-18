# ZeroJS Membrane Geometry — Spec Outline

## 1. Purpose & Scope
Defines the structural geometry of the ZeroJS membrane — the boundary object that separates:
- domain logic (inside the boundary)
- representational logic (outside the boundary)

The membrane ensures reversible, domain‑agnostic, deterministic transitions between layers.

---

## 2. Membrane Model Overview
The membrane is the structural interface between:
- **Boundary Layer** — domain logic, request handling, semantic operations.
- **Representational Domain** — UI primitives, slots, HTML streaming.
- **Courier Model** — the membrane object that carries representational state.

The membrane enforces:
- isolation
- reversibility
- deterministic transitions
- domain‑agnostic semantics

---

## 3. Membrane Laws
The membrane geometry is governed by strict laws:

### 3.1 Isolation Law
Domain logic cannot directly manipulate representational structures.
All domain outputs must pass through the membrane via couriers.

### 3.2 Reversibility Law
Every membrane transition must be invertible.
Courier → Representational → HTML must be reversible.

### 3.3 Determinism Law
Membrane transitions must produce identical outputs for identical inputs.
No global state, no nondeterministic ordering.

### 3.4 Domain-Agnostic Law
Membrane objects cannot encode domain semantics.
They carry structure, not meaning.

---

## 4. Membrane Structure
Defines the structural components of the membrane.

### 4.1 Membrane Context
Metadata required for deterministic transitions:
- requestId
- boundary metadata
- representational metadata

### 4.2 Courier Object
The membrane’s primary carrier of representational state.
Couriers must be:
- reversible
- structurally typed
- boundary‑safe
- domain‑agnostic

### 4.3 Transition Operators
Operators that move data across the membrane:
- `emitCourier`
- `assembleRepresentational`
- `composeSlots`
- `streamHTML`

Each operator must be reversible.

---

## 5. Membrane Lifecycle
Defines the lifecycle of membrane objects.

### 5.1 Creation
Boundary logic emits courier seeds.
Membrane constructs couriers from seeds.

### 5.2 Mutation
Couriers may be structurally transformed but never semantically altered.

### 5.3 Emission
Couriers are emitted into the representational domain.

### 5.4 Destruction
Couriers are destroyed after streaming completion.
No courier may persist across requests.

---

## 6. Membrane Transitions
Defines the reversible transitions across the membrane.

### 6.1 Boundary → Courier
Semantic outputs become courier seeds.
Courier seeds become full couriers.

### 6.2 Courier → Representational
Couriers are transformed into representational primitives:
- nodes
- fragments
- slots

### 6.3 Representational → Slots
Representational primitives are composed into deterministic slot sequences.

### 6.4 Slots → HTML Stream
Slots are emitted as streaming HTML.

### 6.5 HTML → Representational (Reverse)
Defines the reverse mapping required for reversibility guarantees.

---

## 7. Deterministic Ordering Rules
Defines how membrane transitions preserve ordering.

- slot ordering must be stable
- representational assembly must be deterministic
- courier emission must follow structural rules
- streaming must follow slot order exactly

---

## 8. Error Geometry
Defines how errors propagate across the membrane.

### 8.1 Boundary Errors
Converted into representational fallback couriers.

### 8.2 Courier Errors
Converted into structural fallback primitives.

### 8.3 Streaming Errors
Pipeline terminates gracefully with reversible metadata.

---

## 9. Reversibility Guarantees
Defines the formal guarantees of membrane reversibility.

- courier → representational → HTML is invertible
- membrane transitions preserve structural information
- HTML output can reconstruct representational state
- representational state can reconstruct couriers

---

## 10. Glossary References
Links to glossary terms for consistency:
- membrane
- courier
- boundary
- representational domain
- reversible transition
- slot
