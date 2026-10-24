# Selfaware AI 0.1.0 — withdrawn Store proposal

The self-extracting prototype is not a Store-compatible UCP module. This recipe
proposal is withdrawn following maintainer feedback on 24 October 2026.

The working local mod continues separately. A standalone installer/launcher owns
Python extraction, process launch, learning state and logs. The current native
bridge remains a local development component: its file IPC, snapshots and legacy
absolute addresses still disqualify it for Store publication. Moving extraction
out does not by itself make that bridge Store-ready.

A future Store bridge needs in-memory loading, no filesystem access outside its
module directory, no own persistent files/state, reviewed transient IPC and an
inspectable source-to-DLL build. Reuse UCP infrastructure and OpenSHC's typed
resolvers where suitable. Do not re-enable either removed recipe entry before
those requirements are implemented and independently reviewed.

“Selfaware” is the project name. Demonstrated learning currently means measured
model updates and retained observations, not consciousness or generally proven
autonomous self-improvement.
