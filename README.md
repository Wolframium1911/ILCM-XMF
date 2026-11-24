# ILCM-XMF

Experimental Xbox Series compatibility layer research tree. Runs console-targeted
binaries on Windows through a host D3D12 backend and translates console GPU programs
to DXIL. No game files, assets, or title-specific data are included.

## Layout

- `apps/` — command line tools (`translate`, `run`, diagnostics)
- `crates/` — loader, HLE services, GPU back end, shader recompiler, formats
- `tests/`, `xtask/`, `.github/` — tests and development tooling
- `docs/` — architecture notes

## Build

```
cargo build --release -p victory --features diagnostics
```

The runtime points at a user-supplied game directory through `VICTORY_GAME_DIR`;
this repository ships none of it. Cache and data directories are set with
`VICTORY_CACHE_DIR` and `VICTORY_DATA_DIR`.

## Scope and status

Research software. Rendering and interaction with a retail console title are
partial; frame rate is low and lighting is incomplete. See `docs/` for the
architecture. No title names or proprietary assets appear in this tree.

## License

GPL-3.0-or-later (see `LICENSE`). Upstream project credits are in the original
history; this tree is a local working copy prepared for code-only distribution.
