# Case: local patch breaks whole-page scanability

## Input
An existing data dashboard is already readable. A user asks the agent to add a compact comparison for two related metrics beside a chart. The agent adds a new full-width section below the chart, separated by a large gap. Locally the new block looks polished; globally the two metrics are now far apart, the page is longer, and the next action is detached from its evidence.

## Expected behavior
1. Identify the primary scan path, device and which values must be compared side by side.
2. Before modifying, show a space/impact map: remove, merge, move, resize, add, and identify affected neighboring blocks. Do not assume a 100vh limit unless requested.
3. Prefer reusing/rearranging existing space when it improves proximity. If more page length is genuinely justified, explain the trade-off.
4. Render and capture the entire page and first viewport at the primary desktop and mobile sizes **before and after**. At normal zoom, check grouping, alignment, density, color blocks, visual weight, total length and whether compared values fit within a coherent scan path. If screenshots cannot be captured, label visual quality unverified.
5. Run the opposite trap too: an over-compressed revision that makes comparison harder. Do not reward compactness alone.
6. State what was actually tested; an agent's screenshot review is not human usability testing.

## Failure conditions
- Only checks whether the new component itself looks good.
- Adds vertical space without accounting for the displaced content.
- Spreads related data across distant sections, forcing repeated eye travel or scrolling.
- Treats more whitespace or more cards as automatically better.
- Rigidly enforces one-screen height for a task where scrolling is appropriate.

## Evaluation
Human reviewer compares before/after at the same viewport: locate primary question, compare related metrics, find supporting evidence and next action. Record time/eye-travel observations only if actually measured. Pass if the patch improves the task without degrading whole-page coherence.
