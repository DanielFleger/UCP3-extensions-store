# Selfaware AI memory bridge — experimental review proposal

This is community research, not an official or production-ready UCP component.
It replaces the withdrawn self-extracting proposal (#63), which remains closed.
Both recipe entries select a self-contained top-level source folder at the same
explicit commit; the Store build does not package the repository root.

The module is loaded from its ZIP by UCP, including its proxied DLL. It does not
extract or start an external runtime, create command/snapshot files or persist
learning state. Requests, binary snapshots and bounded diagnostics travel through
pagefile-backed memory. The separately installed local application owns journals
and learning data in Documents. It runs without an AI assistant or language model.

The normal external application requires the Store's signed module and preserves
secure mode. The unsigned developer-review application is separately labelled
and intended for an isolated game copy. The Store must not install that review
application as part of the module. Selecting SamurAI without the external app
does not provide a functioning AI controller.

Own code is MIT-licensed. Third-party notices remain; the native build packages
the standard-library notices from the actual Rust toolchain it used.

Validation and limitations are recorded in the pinned source's
`docs/Store-Speicherbruecke.md` and `daten/store_grenze_20261024/`:
native-menu fresh-game takeover at tick zero, two controllers building, binary
snapshots, rejected disk request and restored lobby values. A failed earlier
run is preserved alongside its correction. Supported engine: Crusader 1.41;
version-specific addresses remain and guarded hook signatures are checked.
This is not a complete OpenSHC port or a claim to understand the whole engine.

Maintainer review, signing and agreement on where experimental community
projects belong are required before this proposal becomes public Store content.
