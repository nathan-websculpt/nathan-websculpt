### Hi, I'm Nathan

**As a C#/.NET developer, I am...**

Building ASP.NET Core applications with an emphasis on data integrity, concurrency, testing, and diagnostics.

**As a C++ developer, I am...**

Systems-oriented and focused on deterministic simulation, state management, and production-grade build pipelines.

**My Coding Journey**

I spent almost a decade doing full-stack C#/.NET full time before transitioning into the blockchain space. It was blockchain dev that introduced me to Rust, and that was when I discovered that I love low-level languages. I started writing [Huff](https://github.com/nathan-websculpt/huff-codes), [Rust](https://github.com/nathan-websculpt/rust-codes), [Zig](https://github.com/nathan-websculpt/zig-codes), [C](https://github.com/nathan-websculpt/c-codes), and [C++](https://github.com/nathan-websculpt/cpp-codes) before landing on C++ as my favorite... from there, I started building games. These days I am finding myself coming full-circle, back to C# and .NET, with the specific interest of using my new C++ knowledge to learn the deep internals of how .NET works.

[Email me](mailto:websculpt@proton.me)

## Featured .NET Work

### [Warehouse — Inventory and Transfer Management](https://github.com/nathan-websculpt/warehouse)

**C# · .NET 10 · ASP.NET Core · SQL Server / T-SQL · EF Core · Blazor WebAssembly**

An ongoing multi-tenant inventory system built around keeping stock balances and movement history consistent under concurrent requests and retries.

- **Transfer correctness:** Atomic, idempotent completion using `SERIALIZABLE` transactions, update locks, and `rowversion` checks; completed requests can be replayed without duplicate stock posting.
- **Database integrity:** Tenant-scoped composite unique keys and foreign keys, quantity constraints, and triggers protecting approved and received transfers.
- **API design:** Asynchronous EF Core queries, parameterized stored-procedure calls through Microsoft.Data.SqlClient, ProblemDetails responses, and validated bidirectional cursor pagination with deterministic ordering and supporting indexes.
- **User interfaces:** Blazor WebAssembly and Razor Pages workflows using shared C# contracts and asynchronous HttpClient calls with cancellation support.
- **Operations and diagnostics:** Aspire orchestration, service discovery, HTTP resilience, database readiness checks, and OpenTelemetry logging, metrics, and tracing. A custom SQL trace processor removes query text, parameter tags, and connection-string tags.
- **Testing:** xUnit integration tests through WebApplicationFactory against SQL Server; unit tests for validation, pagination helpers, and asynchronous client state; and bUnit component tests for UI recovery and retained state.

[Explore the repository](https://github.com/nathan-websculpt/warehouse)

## C++ Work

These projects use games as controlled environments for simulation, state management, ownership, and build/release discipline.

**C++ · SDL3 · No Game Engine Used**

### [Garden Sim](https://garden-sim.itch.io/garden-sim)

- Deterministic simulation built without a game engine, with horticulture and botany informing the domain model.
- Windows release pipeline with packaging, dependency staging, and runtime validation.
- Distributed as installable builds through itch.io.

[Download on itch.io](https://garden-sim.itch.io/garden-sim) · [Watch the trailer](https://www.youtube.com/watch?v=NMSl7ALI3FU) · [Read the Garden Story](docs/garden_story.md)

### [Defender](https://github.com/nathan-websculpt/sdl3-defender-v3)

Seedable fixed-step simulation, explicit resource ownership, and recoverable high-score persistence. Includes collision and resource-lifecycle regression tests, plus Windows release tooling with package validation and Unicode-path smoke checks.

### [Arkanoid](https://github.com/nathan-websculpt/sdl3-arkanoid)

SDL-independent simulation core with 120 Hz fixed-step updates and explicit gameplay state transitions. Regression tests verify input edges, collision ordering, and state preservation across resets.

---

<details>
<summary>Earlier blockchain work</summary>

EVM smart contracts and low-level Huff exploration focused on execution behavior, determinism, and correctness.

- [Gospel Onchain](https://github.com/nathan-websculpt/gospel)
- [Council](https://github.com/nathan-websculpt/council)
- [Crowd Fund](https://github.com/nathan-websculpt/crowd-fund-v4)
- [Huff Codes](https://github.com/nathan-websculpt/huff-codes)
- [Blockchain Blog](https://medium.com/@websculpt)

[More on my blockchain work](docs/blockchain.md)

</details>

--- 

## Want to help support my work?

##### [Support Garden Sim](https://ko-fi.com/gardensim)

##### [Donate Crypto](https://etherscan.io/address/0x1e7aAbB9D0C701208E875131d0A1cFcDAba79350)

##### [Send me an Email](mailto:websculpt@proton.me)