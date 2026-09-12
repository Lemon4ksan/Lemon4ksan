# Arseny Komolov

Systems engineer. Focus: low-level network stacks, hardware-accelerated substrates, and protocol engines in Go 1.27+.
Core principles: mechanical sympathy, zero-allocation data paths, and replacing slow runtime abstractions with direct silicon execution (SIMD, Plan 9 assembly, `io_uring`).

## Core Infrastructure

* **[`foundation`](https://github.com/lemon4ksan/foundation)** — Silicon substrate. Native Go 1.27 `simd/archsimd` intrinsics, `c2plan9` (Clang `.o` to Plan 9 ASM compiler), 64-byte cacheline alignment, off-heap memory slabs.
* **[`sein`](https://github.com/lemon4ksan/sein)** — Server network stack & framework. Single-port `:443` multiplexing (H1/H2/H3/gRPC/WS), JIT struct offset DTO compiler, zero-glue domain routing (3.2M+ RPS, 0 allocs).
* **[`aoni`](https://github.com/lemon4ksan/aoni)** — Zero-alloc client transport. Linux `io_uring` engine (2.48M+ RPS), bit-exact Chromium JA4/p0f fingerprinting, ECH, Post-Quantum TLS 1.3 (ML-KEM 768).
* **[`vortex`](https://github.com/lemon4ksan/aoni/tree/main/cmd/vortex)** — AST toolchain. Ingests `.har` traffic dumps, generates zero-alloc clients via 3-Way AST Merge, deobfuscates Google JSPB tuples, runs browser WAF attestation oracles.
* **[`dawn`](https://github.com/lemon4ksan/dawn)** — Database protocol engine. Direct binary wire-to-struct offset streaming bypassing `database/sql` reflection (5–20 µs UDS latency, 0 allocs).

## Applied Tooling

* **[`ao`](https://github.com/lemon4ksan/ao)** — Fork of `curl` replacing the C transport with `libaoni` (9,145+ RPS on 100 threads, JA4 + PQ-TLS).
* **[`g-man`](https://github.com/lemon4ksan/g-man)** — High-concurrency Steam client SDK and trading daemon with raw protobuf socket framing.
* **[`gozip`](https://github.com/lemon4ksan/gozip)** — Parallel, memory-pooled replacement for the standard `archive/zip`.

## Technology Stack

* **Languages & Low-Level:** Go 1.27+, C (LLVM), Plan 9 Assembly, TypeScript.
* **Kernel & Hardware:** Linux `io_uring`, SIMD (AVX2/NEON), Unix Domain Sockets.
* **Protocols & Transport:** HTTP/3 (QUIC), Post-Quantum TLS 1.3, PostgreSQL Wire v3.0, gRPC/Protobuf.

## Contacts

* Telegram: [@LemonadeAK](https://t.me/LemonadeAK)
* Email: [arsenii.komolov@yandex.ru](mailto:arsenii.komolov@yandex.ru)

---

> «Идиот восхищается сложностью, гений восхищается простотой. Физик пытается сделать вещи простыми. Для идиота же — чем сложнее вещь, тем больше он будет ею восхищаться. Если вы сделаете что-то настолько запутанным, что он не сможет этого понять, он подумает, что вы бог…»
