# ZeroJS Glossary (Expanded)

## A

### **[Assembly](ca://s?q=Explain_zeroJS_representational_assembly)**  
The reversible process of converting couriers into representational primitives (nodes, fragments, text blocks). Assembly must be deterministic, domain‑agnostic, and invertible.

### **[Atom](ca://s?q=Explain_zeroJS_representational_domain)**  
The smallest representational primitive in ZeroJS. Atoms include text blocks, structural markers, and minimal nodes.

---

## B

### **[Boundary Layer](ca://s?q=Explain_zeroJS_boundary_layer)**  
The domain logic execution zone. The boundary receives normalized envelopes and emits courier seeds. It cannot manipulate representational structures.

### **[Boundary Metadata](ca://s?q=Explain_zeroJS_request_envelope)**  
Structural metadata attached to envelopes and couriers to preserve lineage and reversibility across membrane transitions.

---

## C

### **[Courier](ca://s?q=Explain_zeroJS_courier_model)**  
The membrane object that carries representational structure across the boundary. Couriers are reversible, domain‑agnostic, and structurally typed.

### **[Courier Seed](ca://s?q=Explain_zeroJS_courier_lifecycle)**  
Minimal structural output emitted by the boundary layer. Seeds become full couriers during membrane construction.

### **[Courier Lineage](ca://s?q=Explain_zeroJS_reversibility)**  
The reversible ordering and ancestry metadata that allows couriers to reconstruct boundary outputs and representational structure.

---

## D

### **[Determinism](ca://s?q=Explain_zeroJS_deterministic_rendering)**  
The substrate law requiring identical inputs to produce identical outputs across all layers. Determinism is essential for reversibility.

### **[Domain-Agnostic](ca://s?q=Explain_zeroJS_foundational_system)**  
A structural constraint: representational primitives, couriers, and slots cannot encode domain semantics.

---

## E

### **[Envelope](ca://s?q=Explain_zeroJS_request_envelope)**  
The normalized, boundary‑safe representation of incoming requests. Envelopes preserve structure, not semantics.

### **[Error Geometry](ca://s?q=Explain_zeroJS_error_geometry)**  
The reversible, deterministic system for handling errors across all layers. Errors become fallback couriers, primitives, or slots.

---

## F

### **[Fragment](ca://s?q=Explain_zeroJS_representational_domain)**  
A reversible grouping of representational nodes. Fragments preserve ordering and structural lineage.

### **[Fallback Structure](ca://s?q=Explain_zeroJS_error_geometry)**  
A reversible substitute produced when errors occur. Fallback couriers, primitives, and slots must preserve lineage.

---

## H

### **[HTML Stream](ca://s?q=Explain_zeroJS_rendering_pipeline)**  
The final output of the rendering pipeline. HTML must preserve enough structure to reconstruct slot boundaries and representational lineage.

### **[Hydration-Free](ca://s?q=Explain_zeroJS_navigation_model)**  
ZeroJS never reconstructs server state on the client. All navigation triggers a fresh representational pipeline.

---

## L

### **[Lineage](ca://s?q=Explain_zeroJS_reversibility)**  
The reversible ancestry metadata that allows reconstruction of ordering, courier structure, and representational primitives.

---

## M

### **[Membrane](ca://s?q=Explain_zeroJS_membrane_geometry)**  
The structural boundary between domain logic and representational logic. The membrane enforces isolation, reversibility, and deterministic transitions.

### **[Membrane Transition](ca://s?q=Explain_zeroJS_membrane_geometry)**  
A reversible transformation across boundary → courier → representational domain.

---

## N

### **[Navigation](ca://s?q=Explain_zeroJS_navigation_model)**  
The deterministic, hydration‑free process of moving between pages. Navigation always enters the boundary via envelope normalization.

### **[Node](ca://s?q=Explain_zeroJS_representational_domain)**  
A representational primitive representing a structural UI element (tag, attributes, children).

---

## P

### **[Pipeline](ca://s?q=Explain_zeroJS_rendering_pipeline)**  
The full reversible chain:  
Envelope → Boundary → Courier → Representational → Slot → HTML.

### **[Primitive](ca://s?q=Explain_zeroJS_representational_domain)**  
A representational unit: node, fragment, text block, or structural marker.

---

## R

### **[Representational Domain](ca://s?q=Explain_zeroJS_representational_domain)**  
The structural UI space where couriers become representational primitives. Domain‑agnostic and reversible.

### **[Reversibility](ca://s?q=Explain_zeroJS_reversibility)**  
The substrate invariant: every transformation must be invertible without loss of structural information.

### **[Request Envelope](ca://s?q=Explain_zeroJS_request_envelope)**  
The normalized structural representation of incoming navigation events.

---

## S

### **[Slot](ca://s?q=Explain_zeroJS_slots_model)**  
A deterministic representational region used for streaming HTML. Slots preserve ordering and lineage.

### **[Slot Composition](ca://s?q=Explain_zeroJS_slots_model)**  
The reversible process of grouping representational primitives into ordered slot sequences.

### **[Streaming](ca://s?q=Explain_zeroJS_rendering_pipeline)**  
The emission of HTML in deterministic slot order. Streaming must be reversible.

---

## T

### **[Text Block](ca://s?q=Explain_zeroJS_representational_domain)**  
A typed representational primitive containing reversible text content.

### **[Transition](ca://s?q=Explain_zeroJS_membrane_geometry)**  
Any reversible movement across substrate layers.

---

## U

### **[UI Graph](ca://s?q=Explain_zeroJS_representational_assembly)**  
The deterministic representational structure produced during assembly before slot composition.

---

## W

### **[Write Boundary](ca://s?q=Explain_zeroJS_rendering_pipeline)**  
The final structural boundary where slots become streaming HTML.

