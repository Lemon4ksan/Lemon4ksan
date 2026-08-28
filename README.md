# Hi, I'm Arseny (Lemon4ksan) 👋

I write low-level network stacks, hardware-accelerated substrates, and protocol engines in **Go 1.27+**. 

I care about mechanical sympathy, zero-allocation data paths, and replacing slow runtime abstractions with direct silicon execution (SIMD, Plan 9 assembly, `io_uring`).

---

### 🌠 Projects & Ecosystem

* 🍏 **[`foundation`](https://github.com/lemon4ksan/foundation)** — The silicon substrate. Native Go 1.27 `simd/archsimd` intrinsics, `c2plan9` (Clang `.o` to Plan 9 ASM compiler), 64-byte cacheline alignment, and off-heap memory slabs.
* ⚡ **[`sein`](https://github.com/lemon4ksan/sein)** — Server network stack & framework. Single-port `:443` multiplexing (H1/H2/H3/gRPC/WS), JIT struct offset DTO compiler, and zero-glue domain routing (3.2M+ RPS, 0 allocs).
* ❄️ **[`aoni`](https://github.com/lemon4ksan/aoni)** — Zero-alloc client transport. Linux `io_uring` engine (2.48M+ RPS), bit-exact Chromium JA4/p0f fingerprinting, ECH, and Post-Quantum TLS 1.3 (ML-KEM 768).
* 🌪️ **[`vortex`](https://github.com/lemon4ksan/aoni/tree/main/cmd/vortex)** — AST toolchain. Ingests `.har` traffic dumps, generates zero-alloc clients via 3-Way AST Merge, deobfuscates Google JSPB tuples, and runs browser WAF attestation oracles.
* 🌅 **[`dawn`](https://github.com/lemon4ksan/dawn)** — Database protocol engine. Direct binary wire-to-struct offset streaming bypassing `database/sql` reflection (5–20 µs UDS latency, 0 allocs).

---

### 📁 Battle-Tested & Practical Code

* 📦 **[ao](https://github.com/lemon4ksan/ao)** — Fork of `curl` with its C transport replaced by `libaoni` (9,145+ RPS on 100 threads, JA4 + PQ-TLS).
* 🤖 **[g-man](https://github.com/lemon4ksan/g-man)** — High-concurrency Steam client SDK and trading daemon with raw protobuf socket framing.
* 🗜️ **[gozip](https://github.com/lemon4ksan/gozip)** — Parallel, memory-pooled replacement for Go's standard `archive/zip`.

---

### 💻 Tech Stack

**Languages & Low-Level:**  
![Go 1.27+](https://img.shields.io/badge/Go_1.27+-%2300ADD8.svg?style=for-the-badge&logo=go&logoColor=white)
![Plan 9 ASM](https://img.shields.io/badge/Plan_9_Assembly-black?style=for-the-badge&logo=assemblyscript&logoColor=white)
![C / LLVM](https://img.shields.io/badge/C_/_LLVM-%2300599C.svg?style=for-the-badge&logo=c&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white)

**Kernel & Hardware Substrate:**  
![Linux io_uring](https://img.shields.io/badge/Linux_io__uring-orange?style=for-the-badge&logo=linux&logoColor=black)
![SIMD AVX2 / NEON](https://img.shields.io/badge/SIMD_AVX2_/_NEON-blueviolet?style=for-the-badge)
![Unix Domain Sockets](https://img.shields.io/badge/Unix_Domain_Sockets-23495d?style=for-the-badge)
![Docker](https://img.shields.io/badge/Docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)

**Protocols & Transport:**  
![HTTP/3 & QUIC](https://img.shields.io/badge/HTTP/3_&_QUIC-0052CC?style=for-the-badge)
![Post-Quantum TLS 1.3](https://img.shields.io/badge/TLS_1.3_/_ML--KEM-success?style=for-the-badge)
![PostgreSQL Wire v3](https://img.shields.io/badge/PostgreSQL_Wire_v3.0-336791?style=for-the-badge&logo=postgresql&logoColor=white)
![gRPC / Protobuf](https://img.shields.io/badge/gRPC_/_Protobuf-red?style=for-the-badge&logo=grpc&logoColor=white)

---

### 📫 Contact

- **Telegram:** [@LemonadeAK](https://t.me/LemonadeAK)
- **Email:** [arsenii.komolov@yandex.ru](mailto:arsenii.komolov@yandex.ru)

---

<div align="center">

_«Идиот восхищается сложностью, гений восхищается простотой. Физик пытается сделать вещи простыми. Для идиота же — чем сложнее вещь, тем больше он будет ею восхищаться. Если вы сделаете что-то настолько запутанным, что он не сможет этого понять, он подумает, что вы бог…»_

</div>
