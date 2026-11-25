# CGBJ — Xbox Series X|S Compatibility Layer for Windows

discord.gg/https://discord.gg/wrVCsFnU9p

**Experimental native execution. Efficient shader compilation. Smarter GPU synchronization.**

CGBJ is an experimental open-source compatibility layer based on XCL, focused on improving graphics pipeline performance, resource management, shader compilation, and GPU synchronization on Windows.

The project explores native x64 execution and independently implemented compatibility mechanisms rather than traditional CPU emulation.

## Development Status

**Experimental — Active Development**

CGBJ is currently under development. Full gameplay compatibility has not yet been established.

## Key Features

| Feature | Status |
|---|---|
| Native x64 execution | Inherited from XCL |
| RDNA2 shader translation | Inherited from XCL |
| DirectX 12 compatibility | Experimental |
| Persistent compute pipeline caching | Tested |
| Two-pass native pipeline caching | Tested |
| Concurrent compilation deduplication | Tested |
| GPU queue synchronization improvements | Tested |
| Critical shader prioritization | Experimental |
| Resource lifetime management | In development |
| Direct DXIL backend evaluation | Experimental |
| Full gameplay compatibility | Not verified |

## Engineering Focus

- Persistent shader and pipeline caching.
- Reduced redundant compilation.
- Critical-path GPU dependency analysis.
- Efficient CPU and GPU synchronization.
- Memory-aware compilation scheduling.
- Offline pipeline preparation.
- Native driver cache validation.
- Reproducible regression testing.

## Experimental Performance Results

The following results were reported during development of the compatibility-layer prototype.

| Benchmark | Before | After |
|---|---:|---:|
| Two-pass native pipeline creation | 25.21 s | 0.61 s |
| Selected shader preparation | 25.9 s | 1.0 s |
| Individual native PSO creation | 17.6 s | 0.26 ms |
| Concurrent compilation of an identical pipeline | 3 jobs | 1 job |

These measurements represent selected compilation and cache operations, not overall gameplay performance.

## Development Principles

- Correctness before performance.
- Evidence-driven debugging.
- Reproducible benchmarks.
- Minimal redundant computation.
- No artificial compatibility claims.
- No skipped operations presented as successful execution.

## Target Environment

- Windows 10 / 11 x64
- Rust stable toolchain
- DirectX 12 compatible GPU
- Shader Model 6.6
- DirectX Shader Compiler (DXC)

Hardware and driver compatibility may vary.

## Roadmap

- [x] Persistent native compute cache
- [x] Two-pass pipeline cache integration
- [x] Duplicate compilation prevention
- [x] GPU dependency diagnostics
- [x] Experimental queue synchronization improvements
- [ ] Extended memory management
- [ ] Shader execution equivalence validation
- [ ] Gameplay compatibility validation
- [ ] Cross-vendor GPU testing
- [ ] Performance and stability optimization

## Legal and Usage Notice

CGBJ is an independent compatibility-layer research project based on XCL.

https://discord.gg/wrVCsFnU9p

The project is not affiliated with, endorsed by, or sponsored by Microsoft, Xbox, or any game publisher.

Users are responsible for complying with applicable laws and software license agreements.

The project is intended for interoperability research and use with lawfully obtained software. Unauthorized game distribution, proprietary SDK redistribution, and circumvention of access controls are outside the intended scope of this project.

## Credits

CGBJ builds upon the work of the XCL project and its contributors.

Upstream: https://github.com/xcl-dev/xcl

Original copyright notices and applicable third-party license requirements must be preserved.

## License

GPL-2.0-only for the XCL-derived source tree, subject to applicable third-party licensing requirements.

See LICENSE and THIRD_PARTY.md for details.

---

**CGBJ — Compiling Games Before Judgment.**

*Correctness first. Performance follows.*
