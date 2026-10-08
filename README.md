<p align="center">
  <img src="https://raw.githubusercontent.com/godotbridge/addon/main/icon.png" width="128" height="128" alt="GodotBridge icon" />
</p>

<h1 align="center">GodotBridge</h1>

<p align="center">
  <strong>AI control for the Godot editor and your running game.</strong><br/>
  345 tools &middot; 36 categories &middot; Godot 4.x &middot; live-verified
</p>

<p align="center">
  <a href="https://pypi.org/project/godotbridge/"><img src="https://img.shields.io/pypi/v/godotbridge?label=PyPI&color=blue" alt="PyPI version"></a>
  <a href="https://godotengine.org/asset-library/asset"><img src="https://img.shields.io/badge/Godot-Asset%20Library-blue?logo=godot-engine" alt="Godot Asset Library"></a>
  <a href="https://godotbridge.dev"><img src="https://img.shields.io/badge/web-godotbridge.dev-blue" alt="Website"></a>
</p>

---

GodotBridge is an MCP server that lets Claude, Cursor, Windsurf, or any MCP-speaking AI agent inspect and control a real Godot 4.x editor session and the game it's running — build scenes, write scripts, wire up physics and shaders, then press Play and watch, debug, and fix the result.

## Quick start

```bash
pip install godotbridge
```

**1. Install the Godot addon** — from the [Godot Asset Library](https://godotengine.org/asset-library/asset) (search "GodotBridge") or [GitHub](https://github.com/godotbridge/addon)

**2. Register with your AI client:**

| Client | Command |
|--------|---------|
| Claude Code | `claude mcp add godot-bridge --scope user -- godotbridge` |
| Claude Desktop | Add `{"command": "godotbridge"}` to `claude_desktop_config.json` |
| Cursor | Add `{"command": "godotbridge"}` to `.cursor/mcp.json` |
| Windsurf | Add `{"command": "godotbridge"}` to MCP config |

**3. Start building** — open a session in your Godot project folder.

## How it works

```
Your AI agent (Claude, Cursor, etc.)
        │
        │  MCP / stdio
        ▼
GodotBridge MCP Server (Python)
        │
        │  WebSocket · ws://127.0.0.1:8765
        ▼
Godot editor addon (GDScript)
        │
        │  WebSocket · ws://127.0.0.1:8766
        ▼
Your running game (runtime probe)
```

## What's included

| Tier | Tools | Categories | Price |
|------|-------|------------|-------|
| **Lite** | 67 | 12 | Free forever |
| **Full** | 345 | 36 | $29 one-time |

**Lite** covers scene analysis, file operations, editor interaction, project health, input setup, signals/groups, and more.

**Full** adds scene construction, animation systems, rigging, shader authoring, runtime game control, AI Image Studio, physics, navigation, multiplayer, and everything else.

## Links

- [Website](https://godotbridge.dev) — features, pricing, docs
- [PyPI](https://pypi.org/project/godotbridge/) — `pip install godotbridge`
- [Godot Addon](https://github.com/godotbridge/addon) — editor plugin source
- [Releases](https://github.com/godotbridge/releases) — changelog and downloads
- [Report Issues](https://github.com/godotbridge/releases/issues)

## License

The Godot editor addon is MIT licensed. The MCP server is proprietary — free Lite tier, paid Full tier.

---

<p align="center">
  Built by <a href="https://digital-fusion.com.tr">DigitalFusion</a>
</p>
