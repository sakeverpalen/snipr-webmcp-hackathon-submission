# SNIPR WebMCP Hackathon Submission

SNIPR WebMCP demonstrates how an AI assistant can safely interact with a real renovation workflow through WebMCP.

The demo connects four things that normally live in separate places:

- Structured assignment context
- Map and 3D room evidence
- Product specifications attached to room elements
- Human approval before operational write actions

## Demo

Live demo:

https://webmcp.snipr.nl

Video demo:

Paste the final unlisted YouTube URL here.

Demo credentials, if needed:

```text
Email: demo@snipr.nl
Password: snipr-demo-2026
```

Suggested prompts:

```text
Which shower mixer belongs to the bathroom of this assignment?
```

```text
Find the first available inspection slot.
```

## What It Shows

In the demo, a contractor asks which shower mixer belongs to a bathroom assignment.

SNIPR WebMCP reads the selected assignment, address, room data, and resident choices. It returns the exact product answer and lets the user verify that answer in the normal SNIPR workflow: execution map, 3D building view, bathroom model, and element specifications.

The demo also shows controlled writes. WebMCP can propose an operational action, but SNIPR requires explicit human approval before changes are written back.

## Why WebMCP Matters Here

WebMCP is valuable because it lets the AI assistant work with the existing operational source of truth instead of relying on copied context or loose prompts.

For SNIPR, that means the assistant can help users navigate, verify, and act inside the real renovation workflow while the product remains in control of permissions, data, and write safety.

## Built With

- WebMCP
- Nuxt
- Vue
- TypeScript
- Node.js
- Three.js
- MapLibre
- OpenStreetMap
- Playwright
- FFmpeg
- OpenAI tooling

## Repository Scope

This public repository intentionally does not contain the proprietary SNIPR application source code.

It contains only submission material:

- Project description
- Architecture summary
- Sanitized WebMCP example
- Demo instructions

The production SNIPR codebase remains private.
