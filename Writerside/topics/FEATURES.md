# HelixCore — Feature Overview

A modular, performance-focused Minecraft server core plugin for Paper/Spigot forks.  
HelixCore delivers a unified, extensible toolkit for player features, staff tools, integrations, and future web sync.

[Project repository](https://github.com/your-org/HelixCore)

---

## Table of Contents

- [Summary](#summary)
- [Highlights](#highlights)
- [Features](#features)
  - [Core](#core)
  - [Player Tools & QoL](#player-tools--qol)
  - [Staff & Operator Tools](#staff--operator-tools)
  - [Enhancements & Aesthetics](#enhancements--aesthetics)
  - [Security & Integrations](#security--integrations)
  - [Developer & Server Owner Tools](#developer--server-owner-tools)
  - [Web Integration (Planned)](#web-integration-planned)
- [Installation](#installation)
- [Configuration Example](#configuration-example)
- [Command Examples](#command-examples)
- [Roadmap](#roadmap)
- [Contributing](#contributing)
- [License](#license)

---

## Summary

HelixCore is a single, modular plugin providing essential server functionality—homes, warps, messaging, staff tools—with optional integrations (LuckPerms, PlaceholderAPI, Vault) and planned web sync for tickets and infractions.  
Designed for performance, flexibility, and ease of use.

## Highlights

- Modular: toggle modules in the config
- LuckPerms: advanced permission and rank support
- MiniMessage/Adventure: modern, rich chat formatting
- Async operations and caching for performance
- Optional web integration (MySQL-backed sync for tickets/infractions)

---

## Features

### Core

- Modular architecture — enable/disable modules per server
- Command aliasing for quick remaps
- Lightweight caching and async tasks
- API/hooks for custom modules and integrations
- Live reload (`/core reload`) for config and modules

### Player Tools & QoL

- `/home`, `/sethome` — personal teleport management
- `/warp`, `/setwarp` — shared server warps
- `/spawn`, `/setspawn` — spawn management
- `/msg`, `/reply`, `/ignore` — private messaging with ignore support
- `/nickname`, `/realname` — nickname management
- `/playtime` — view total playtime
- `/back` — return to last death or location
- `/tpa`, `/tpahere`, `/tpaccept`, `/tpdeny` — teleport requests
- `/ticket create|open|status|reply|close` — in-game ticketing
- Join & leave messages — configurable per group or player
- Optional Vault hooks for economy

### Staff & Operator Tools

- `/vanish` — staff invisibility
- `/freeze` — freeze players
- `/inspect`, `/invsee`, `/endersee` — inventory management
- `/broadcast` — formatted global messages
- `/whois` — player details (UUID, IP*, rank, location)
- `/mute`, `/unmute`, `/kick`, `/ban`, `/tempban` — moderation
- `/report` — player reporting with staff notifications
- `/clearinv`, `/heal`, `/feed`, `/fly`, `/gamemode` — staff utilities
- `/tp`, `/tpall`, `/tppos`, `/teleport` — advanced teleport tools
- `/staffchat` — private staff channel

> *IP visibility depends on server policy and privacy compliance.

### Enhancements & Aesthetics

- MiniMessage (Adventure) support for rich chat (hover, click, colors)
- MOTD & tablist customization (dynamic placeholders)
- Scoreboard/actionbar for live stats
- Announcements (timed or event-driven)
- Join alerts for staff
- Fully configurable custom commands (no coding required)

### Security & Integrations

- Region protection hooks (WorldGuard/Factions)
- Alt-account detection
- Data logging (joins, mutes, bans, teleports, etc.)
- Auto-save & backup for plugin data
- Permission debug command
- MySQL/MariaDB support for persistence and web sync

### Developer & Server Owner Tools

- Stable API for modules and commands
- PlaceholderAPI integration
- Configurable command cooldowns and limits
- Admin utilities: reload, diagnostics, permission checks

---

## Web Integration (Planned)

HelixCore's web integration will connect in-game systems with a standalone web panel (PHP/HTML/JS) using a shared database.  
This is optional and can be disabled in the config.

**Planned web features:**

- Tickets: create/manage support tickets from web or in-game
- Infractions & history: centralized bans, mutes, warnings
- Account linking: connect Minecraft and web accounts
- Optional 2FA or web tokens for secure actions
- MySQL/MariaDB compatibility and configurable connection

**Architecture:**

- Website runs separately, syncing via database
- Web sync can be enabled/disabled per server

---

## Installation

1. Place `HelixCore.jar` in your server's `plugins/` folder.
2. Start the server to generate configuration files.
3. Configure modules and integrations as needed.

---

## Configuration Example

```yaml
modules:
  player-tools: true
  staff-tools: true
  web-sync: false

database:
  type: mysql
  host: localhost
  port: 3306
  database: helix
  username: helix_user
  password: supersecurepassword
```

After editing `config.yml`, use `/core reload` or restart the server.

---

## Command Examples

- `/home [player]`
- `/sethome [name]`
- `/warp [name]`
- `/ticket create <subject>`
- `/core reload`

See plugin help or `plugin.yml` for a full command list.

---

## Roadmap

Planned and upcoming features:

- Kits & rewards
- Daily login bonuses
- Chat filtering & anti-swear
- Advanced ticket dashboard
- Warp & portal GUI
- Web analytics for player activity

---

## Contributing

Contributions are welcome!  
Please open an issue for major changes, fork the repo, and submit pull requests with clear descriptions.

---

## License

MIT License. See `LICENSE` for details.

---

