# Selfaware AI 0.1.0 — review candidate

Adds the Content entry **Selfaware AI** and its `selfaware-runtime` dependency
for UCP 3.0.7 / Crusader 1.41 on 64-bit Windows. Both entries pin the same source
commit. The plugin selects SamurAI in the Abbot slot; it does not replace the
other configured lords.

The module bundles the existing kernel 19, native bridge and a hash-pinned
portable Python runtime. It starts the local controller with the game; no LLM
service, supervising assistant or separate Python installation is required.
The existing online learner persists measured loss/movement rates. A match
journal records observations, native outcomes and explicitly unverified aborts.
Learning state is separated by effective UCP configuration and runtime revision.
No tactical-policy optimization is included in this packaging change.

The candidate also exposes editable starting troop counts under Customisations:
four assassins and six Arabian archers by default, replacing the inherited Abbot
troops. Other AI slots retain their rosters. Native reads verified all three
start modes and an alternate 2-assassin/8-archer configuration. The preset is a
proposed starting point, not a demonstrated balance result. Local bootstrap no
longer depends on PowerShell module autoloading and writes per-game startup logs.

Validation: ordinary secure game startup after removing the unavailable legacy
development module; unsigned isolated package launch; fresh match through native
menu handlers; two autonomous controllers; persisted learning and honest aborted
match receipts. Reproducible evidence is in the pinned source under
`daten/installation_20261024/`. No screenshots are included.
Additional fresh-match, startup counterexample and native roster evidence is in
`daten/starttruppen_20261024/`. Windows package build 40087556860 passed.

## Release gate

This is a draft submission. Before publishing:

- Complete module build/signature review with the Store's trusted signer.
- Verify Store installation resolves both entries and shows Selfaware AI in Content.
- Run a fresh menu match with secure mode enabled and no development folder/runtime.
- Review the local command bridge and external worker execution as trusted module behavior.

Unsigned development tests are not proof of secure-mode compatibility. This PR
must not be described as already released/installable from the official Store.
