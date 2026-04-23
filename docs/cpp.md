## C++ Systems Approach

These projects use small games as controlled environments to explore deterministic simulation, state management, and system boundaries.

---

### Core Principles

- Deterministic fixed-step simulation (no frame-rate dependence)
- Explicit ownership and mutation boundaries
- Centralized orchestration of simulation
- Rendering treated as a read-only consumer of state

---

### Why Games?

Games provide a constrained environment where:

- update ordering must be precise
- state transitions must be explicit
- nondeterminism is immediately visible
- systems can be reasoned about frame-by-frame

---

### Simulation Model

- Fixed timestep loop
- Stable update ordering
- Explicit state machine phases
- Controlled mutation paths

Focus:
- reproducibility  
- predictability  
- testability  

---

### Ownership + Mutation

- Gameplay state owned centrally
- Mutation occurs in controlled update paths
- Rendering does not mutate gameplay state
- Separation between simulation and presentation

---

### Build + Release Pipeline

- CMake preset-driven builds
- vcpkg dependency management
- Windows-focused packaging
- Runtime dependency staging and filtering
- Install tree vs build tree separation
- Runtime validation gates

Goals:
- reproducible builds  
- consistent environments  
- fail-closed validation  

---

### Projects

#### Garden Sim (Primary System)

- full deterministic simulation system (no engine)
- real-world packaging and distribution (itch.io)
- fail-closed Windows build configuration (toolchain + triplet required)
- preset-driven builds (VS 18 2026 + vcpkg manifest mode)
- runtime dependency staging (DLL filtering, system exclusion)
- asset installation + build-tree staging
- separate runtime vs testing path policies
- multi-layer test coverage (core, save/load, runtime gates)

Focus:
- correctness under real distribution constraints  
- reproducible builds across environments  
- validation of packaged artifacts, not just local runs  

---

#### Defender

- system-level refactor
- ownership boundary enforcement
- centralized simulation orchestration
- simulation/render separation

---

#### Arkanoid

- minimal deterministic simulation slices
- incremental system construction
- strict control over update flow

---

### Takeaway

The focus is not the game itself, but:

- deterministic behavior  
- explicit system design  
- controlled execution  
- reproducible builds and validated artifacts  

These patterns translate directly to non-game systems.