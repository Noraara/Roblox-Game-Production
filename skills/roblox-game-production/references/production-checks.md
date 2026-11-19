# Match the check to the Roblox feature

| Boundary | What to verify |
| --- | --- |
| Client and server | Keep authoritative progression on the server. Check accepted and rejected behavior in a disposable local test. Verify the final committed state and the feedback derived from it. |
| Persistence and economy | Preserve stable save IDs and old profile shapes. Verify interrupted, repeated and concurrent actions where relevant. A backend error or rejected action must leave state consistent. Use disposable data for engine-backed checks. Use current platform policy for monetization and report any compliance check that still needs a real test. |
| UI and input | Verify keyboard, touch, gamepad focus and safe insets as applicable. Check focus restoration if the invoking row disappears and check text overflow for the expected locale. Keep visual review within project permissions. |
| Assets and scene | Verify intended destination, scale, axes, pivot, collision, materials, and asset loading after import. For rigs or motion check relevant poses and ownership. |
| Performance | Establish a warmed baseline in the same scene and device class. Compare the same workload after the change. For suspected leaks, check whether memory remains elevated after teardown and identify its owner. |
| Debugging | Trace the signal across its real execution contexts. For a missing asset, distinguish ownership, actual load and the final consumer. Change one relevant variable at a time when diagnosing a scoped failure. |

Project fixtures and specialist skills deepen these checks when installed. Packaging, replication, runtime, device input and final approval are distinct observations. Record the check actually run and the build or session where it ran.
