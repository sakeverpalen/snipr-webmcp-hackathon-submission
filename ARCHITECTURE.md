# Architecture Summary

This submission is based on a private SNIPR implementation. The architecture below describes the integration without exposing proprietary source code.

## High-Level Flow

1. The user opens a renovation assignment in SNIPR.
2. The embedded assistant uses WebMCP tools to retrieve structured context.
3. SNIPR returns scoped assignment data such as address, rooms, resident choices, planning status, and element specifications.
4. The user can verify the answer visually through the map and 3D room view.
5. If the assistant proposes a write action, SNIPR shows a human approval dialog before applying the change.

## Context Sources

The WebMCP layer can expose scoped, task-relevant data from SNIPR:

- Assignment metadata
- Address and geospatial context
- Room information
- Resident choices
- Product/catalog selections
- Planning availability
- Communication status
- Documents and inspection progress

## Read Versus Write

Read operations can return contextual information immediately when the user has access to the selected assignment.

Write operations are treated differently:

- The assistant proposes an action.
- SNIPR explains the exact operation.
- The user explicitly confirms or cancels.
- SNIPR records the resulting action in the normal workflow.

## Demo Scenario

The demo focuses on one realistic contractor question:

```text
Which shower mixer belongs to the bathroom of this assignment?
```

The answer is verified through:

- Assignment context
- Bathroom room data
- Resident product choices
- 3D room visualization
- Element-level product labels

Then the demo shows a controlled planning action:

```text
Find the first available inspection slot.
```

This demonstrates that WebMCP can help with operational actions while SNIPR remains the source of truth.
