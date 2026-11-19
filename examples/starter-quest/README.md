# Starter quest delivery example

A fictional experience invites a new player to activate a beacon. The server marks the quest complete once and grants one starter badge flag in the player’s existing progression record. The UI shows completion from the committed server state. This is a worked verification plan for a feature, with expected outcomes.

## Trace the owners

| Concern | Owner |
| --- | --- |
| Player-visible beacon and interaction prompt | The place file, if the project owns its scene there. |
| Completion and eligibility | The project’s existing server quest service. |
| Persisted badge flag | The existing progression transaction or save owner. |
| Success and retry feedback | The quest UI observing the committed result. |

## Verify the feature

| Test | Expected result | Where to check |
| --- | --- | --- |
| Eligible player completes the quest | The quest and badge flag are recorded together and the client shows completion. | Focused state check, then a permitted Studio session. |
| Player retriggers the quest | Completion remains recorded and the badge flag does not change again. | Local state fixture and disposable Studio profile if available. |
| Persistence temporarily fails | The UI does not report a grant as complete. The state remains consistent and retryable. | Failure fixture against the project's persistence boundary. |
| Player rejoins after the successful grant | The saved completion and badge flag are restored. | Authorized disposable profiles in the intended test environment. |

If Studio is unavailable, complete source and fixture checks that can run, then record runtime, replication and rejoin as unverified. Resume by opening the exact test place and loading the disposable profile. Record the checks that actually run.
