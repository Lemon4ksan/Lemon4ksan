# Arseny Komolov

Systems engineer. Focus: low-level network stacks, hardware-accelerated substrates, and protocol engines in Go 1.27+.
Core principles: mechanical sympathy, zero-allocation data paths, and replacing slow runtime abstractions with direct silicon execution (SIMD, Plan 9 assembly, `io_uring`).

## Core Infrastructure

* **[`foundation`](https://github.com/lemon4ksan/foundation)** — Silicon substrate. Native Go 1.27 `simd/archsimd` intrinsics, 64-byte cacheline isolation, off-heap memory slabs (`silicon/pool`, `borrow`, `urlkit`).
* **[`mach`](https://github.com/lemon4ksan/mach)** — Aerodynamic Layer 7 protocol engine. 2.8M+ RPS HTTP/1.1, in-situ HTTP/2 binary overlay (0.49 ns/op, 0 allocs), clean-room RFC 9000/9114 QUIC & HTTP/3, 50.3 GB/s SWAR WebSocket masking, Extended CONNECT (RFC 8441/9220), zero-alloc SOCKS5 dialer.
* **[`seal`](https://github.com/lemon4ksan/seal)** — Ultra-fast containerization & archive engine. Next-gen `eon` format, Cauchy Reed-Solomon $GF(2^8)$ self-healing, $O(1)$ LBA seeking, deterministic memory ceiling ($\le 32$ MB RAM), zero-alloc stream parsers.
* **[`ctrl`](https://github.com/lemon4ksan/ctrl)** — Zero-dependency CLI application framework & hardware-efficient terminal UI toolkit. POSIX flag clumping (`argkit`), Levenshtein typo suggestions, lock-free `NO_COLOR` toggles, zero-alloc `VisibleWidth`, auto-aligned tables, boxes, progress bars.
* **[`sein`](https://github.com/lemon4ksan/sein)** — Server network stack & framework. Single-port `:443` multiplexing (H1/H2/H3/gRPC/WS), JIT struct offset DTO compiler, zero-glue domain routing (3.2M+ RPS, 0 allocs).
* **[`aoni`](https://github.com/lemon4ksan/aoni)** — Zero-allocation client transport. Linux `io_uring` engine (2.48M+ RPS), bit-exact Chromium JA4/p0f fingerprinting, ECH, Post-Quantum TLS 1.3 (ML-KEM 768), transparent RFC 3986 BaseURL resolution.
* **[`vortex`](https://github.com/lemon4ksan/vortex)** — AST toolchain. Ingests `.har` traffic dumps, generates zero-alloc clients via 3-Way AST Merge, deobfuscates Google JSPB tuples, runs browser WAF attestation oracles.
* **[`dawn`](https://github.com/lemon4ksan/dawn)** — Database protocol engine. Direct binary wire-to-struct offset streaming bypassing `database/sql` reflection (5–20 µs UDS latency, 0 allocs).

## Applied Tooling & Compilers

* **[`c2plan9`](https://github.com/lemon4ksan/c2plan9)** — Transpiler pipeline compiling C and LLVM IR to Go Plan 9 assembly for embedding zero-overhead C kernels into pure Go binaries without CGO.
* **[`ao`](https://github.com/lemon4ksan/ao)** — Fork of `curl` replacing the C transport with `libaoni` (9,145+ RPS on 100 threads, JA4 + PQ-TLS).
* **[`g-man`](https://github.com/lemon4ksan/g-man)** — High-concurrency Steam client SDK and trading daemon with raw protobuf socket framing.

## Technology Stack

* **Languages & Low-Level:** Go 1.27+, C (LLVM), Plan 9 Assembly, TypeScript.
* **Kernel & Hardware:** Linux `io_uring`, SIMD (AVX2/NEON), 64-bit SWAR, 64-byte Cacheline Alignment, Off-Heap Slabs.
* **Protocols & Transport:** HTTP/3 (RFC 9000/9114 QUIC), HTTP/2, HTTP/1.1, Post-Quantum TLS 1.3 (ML-KEM 768), RFC 8441/9220 Extended CONNECT, PostgreSQL Wire v3.0, gRPC/Protobuf.
* **Storage & Resiliency:** EON Container Format, Cauchy Reed-Solomon $GF(2^8)$, Trellis-Optimal PRZM, Zero-Alloc Streaming VFS.

## Contacts

* Telegram: [@LemonadeAK](https://t.me/LemonadeAK)
* Email: [arsenii.komolov@yandex.ru](mailto:arsenii.komolov@yandex.ru)

---

> «Идиот восхищается сложностью, гений восхищается простотой. Физик пытается сделать вещи простыми. Для идиота же — чем сложнее вещь, тем больше он будет ею восхищаться. Если вы сделаете что-то настолько запутанным, что он не сможет этого понять, он подумает, что вы бог…»
