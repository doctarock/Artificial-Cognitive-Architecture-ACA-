# Artificial Cognitive Architecture (ACA)

A cognitive-architecture experiment: a continuously running "cognitive loop"
(ACT-R-style memory activation/decay, SOAR-style impasse handling, active
inference-flavored attention) built on top of a tiered pool of local/LAN
language models, plus a real-time 3D visualization of what it's doing.

This repository intentionally contains **no source code** — only compiled,
ready-to-run builds, published under **Releases**. This is a personal
project I'm not ready to open-source yet, but wanted to let people try.

## Setup

1. Go to [Releases](../../releases/latest) and download:
   - **`omega-acad-windows.zip`** — the engine. This is the core daemon:
     the cognitive loop, a local HTTP+WebSocket API, and an MCP server.
     (Windows only for now.)
   - The visualization client for your OS: **`omega-viz-windows.zip`**,
     **`omega-viz-linux.zip`**, or **`omega-viz-macos.zip`**. This is the
     3D viewer — optional, but it's the easiest way to actually watch the
     engine think.
2. Extract `omega-acad-windows.zip` to its own folder, and extract the viz
   zip to another folder.
3. **Start the engine first.** In the engine's folder, just run
   `omega-acad.exe` (double-click, or from a terminal). No setup is
   required to see it come up — with no configuration at all it starts
   with safe built-in fallbacks (no real model calls, a fresh empty local
   database) and begins listening on `http://127.0.0.1:8787`.
   - To connect it to real language models, copy `.env.example` (included
     in the zip) to `.env` in the same folder and fill in your own model
     server(s) — local Ollama/llama.cpp, or a hosted OpenAI-compatible
     endpoint — then restart it. Every setting is commented and optional.
4. **Then start the visualization.** On Linux, `chmod +x omega-viz.x86_64`
   first. It connects automatically to the engine on `127.0.0.1:8787` —
   just launch it while the engine from step 3 is still running.
5. Type into the engine's own console window (or use the visualization) to
   talk to it.

Known limitation: the visualization's "Run Tests" panel won't work — it
talks to a dev-only endpoint that isn't included in this build. Everything
else works normally.

## What's *not* here

No source, no personal data, no API keys or model-server addresses of
mine, and no license — please don't redistribute or modify what you
download without asking first.

The external voice service that I use to hear and speak to this agent is not included either.
