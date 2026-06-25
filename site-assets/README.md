# site-assets

Static files that opencode serves from `https://opencode.ai/` and that the
opencode CLI/TUI may fetch at runtime. Mirrored here so opencode can be used on
a machine that cannot reach `opencode.ai`.

| File | Source URL | What it is |
| --- | --- | --- |
| `config.json` | <https://opencode.ai/config.json> | JSON Schema for `opencode.json` config |
| `theme.json` | <https://opencode.ai/theme.json> | JSON Schema for custom themes |
| `tui.json` | <https://opencode.ai/tui.json> | JSON Schema for TUI config / keybinds |
| `openapi.json` | <https://opencode.ai/openapi.json> | OpenAPI spec for the opencode server API |
| `changelog.json` | <https://opencode.ai/changelog.json> | Release changelog data |
| `install.sh` | <https://opencode.ai/install> | The install script (`curl … | bash`) |

Fetched on 2026-06-24.

## Not mirrored (live services — cannot be made static)

These require the real opencode backend and won't work offline by copying files:

- `api.opencode.ai`, `app.opencode.ai`, `console.opencode.ai` — accounts, auth,
  device login (`/auth/device/code`), billing/workspace endpoints.
- `opencode.ai/zen/*` — the Zen model proxy (routes model requests).
- `opencode.ai/data/` — the hosted stats dashboard web app.
- `/share`, `/proxy/*` — session sharing and proxy connections.

If your machine is firewalled from `opencode.ai`, the features behind those URLs
(Zen models, cloud auth, sharing) need the domain reachable or a configured
proxy — they can't be replaced by these files. Self-hosted/local models and
local config/themes do not depend on the network.
