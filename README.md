# Artificial Cognitive Architecture (ACA)

A cognitive-architecture experiment: a continuously running "cognitive loop"
(ACT-R-style memory activation/decay, SOAR-style impasse handling, active
inference-flavored attention) built on top of a tiered pool of local/LAN
language models, plus a real-time 3D visualization of what it's doing.

This repository intentionally contains **no source code** — only compiled,
ready-to-run builds, published under **Releases**. This is a personal
project I'm not ready to open-source yet, but wanted to let people try.

## Get it

See the [Releases](../../releases) page for downloads:

- **`omega-acad-windows.zip`** — the engine (Windows). This is the core
  daemon: the cognitive loop, a local HTTP+WebSocket API, and an MCP
  server. Runs standalone from a terminal or by double-clicking.
- **`omega-viz-windows.zip`** / **`omega-viz-linux.zip`** /
  **`omega-viz-macos.zip`** — the 3D visualization client (Godot). Connects
  to a running engine on `127.0.0.1:8787`.

Each zip includes its own short README with run instructions. The engine
package includes a `.env.example` — copy it to `.env` to point the engine
at your own model servers (local Ollama/llama.cpp, or a hosted
OpenAI-compatible endpoint), your own PDF library folder, etc. It also runs
with no configuration at all, using safe placeholder fallbacks, so you can
see it come up before wiring in any model.

## What's *not* here

No source, no personal data, no API keys or model-server addresses of
mine, and no license — please don't redistribute or modify what you
download without asking first.
