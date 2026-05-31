# pleme-closedaxis-derive

allvariants targeting the shikumi ClosedAxis trait: for a unit enum, emits the inherent pub const ALL plus impl shikumi::ClosedAxis for Self bound to the same slice, so the enum plugs into shikumi axis_iter / axis_cardinality / ProductCube with zero hand-written ALL. Delegates emission to the proven EnumFold emitter. Consumer enum must derive Copy + Eq + Hash.

[![Build](https://github.com/pleme-io/pleme-closedaxis-derive/actions/workflows/auto-release.yml/badge.svg)](#)
[![crates.io](https://img.shields.io/crates/v/pleme-closedaxis-derive.svg)](https://crates.io/crates/pleme-closedaxis-derive)

## Install

```toml
[dependencies]
pleme-closedaxis-derive = "*"
```

## Generation

This crate is mechanically emitted by [`tatara-rust-ast`](https://github.com/pleme-io/tatara-rust-ast). The author surface is a typed `(defmacro …)` Spec — the proc-macro implementation, tests, Nix flake, caixa wrapper, and CI workflow are all generated. See the catalog at `catalog.json` in the parent registry.
