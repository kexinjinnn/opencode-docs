# opencode.json / opencode.jsonc field reference

Auto-generated from the mirrored schema in [site-assets/config.json](./site-assets/config.json).
See [examples/opencode.jsonc](./examples/opencode.jsonc) for a worked, commented example,
and [docs/config.mdx](./docs/config.mdx) for the full prose docs.

Config is loaded from `~/.config/opencode/opencode.json` (global), then
`opencode.json[c]` and `opencode.local.json[c]` in the project (later wins).

| Field | Type | Notes |
| --- | --- | --- |
| `$schema` | string | JSON schema reference for configuration validation |
| `shell` | string | Default shell to use for terminal and bash tool |
| `logLevel` | LogLevel | Log level |
| `server` | ServerConfig | Server configuration for opencode serve and web commands |
| `command` | object | Command configuration, see https://opencode.ai/docs/commands |
| `skills` | object | Additional skill folder paths |
| `references` | object | Named git or local directory references |
| `reference` | object | **deprecated** — Use 'references' field instead. Named git or local directory references |
| `watcher` | object |  |
| `snapshot` | boolean | Enable or disable snapshot tracking. When false, filesystem snapshots are not recorded and undoing or reverting will not undo/redo file changes. De... |
| `plugin` | array<any> |  |
| `share` | string | Control sharing behavior:'manual' allows manual sharing via commands, 'auto' enables automatic sharing, 'disabled' disables all sharing Values: `ma... |
| `autoshare` | boolean | **deprecated** — Use 'share' field instead. Share newly created sessions automatically |
| `autoupdate` | boolean / string | Automatically update to the latest version. Set to true to auto-update, false to disable, or 'notify' to show update notifications |
| `disabled_providers` | array<string> | Disable providers that are loaded automatically |
| `enabled_providers` | array<string> | When set, ONLY these providers will be enabled. All other providers will be ignored |
| `model` | string | Model to use in the format of provider/model, eg anthropic/claude-2 |
| `small_model` | string | Small model to use for tasks like title generation in the format of provider/model |
| `default_agent` | string | Default agent to use when none is specified. Must be a primary agent. Falls back to 'build' if not set or if the specified agent is invalid. |
| `username` | string | Custom username to display in conversations instead of system username |
| `mode` | object | **deprecated** — Use `agent` field instead. |
| `agent` | object | Agent configuration, see https://opencode.ai/docs/agents |
| `provider` | object | Custom provider configurations and model overrides |
| `mcp` | object | MCP (Model Context Protocol) server configurations |
| `formatter` | boolean / object | Enable or configure formatters. Omit or set to false to disable, true to enable built-ins, or an object to enable built-ins with overrides. |
| `lsp` | boolean / object | Enable or configure LSP servers. Omit or set to false to disable, true to enable built-ins, or an object to enable built-ins with overrides. |
| `instructions` | array<string> | Additional instruction files or patterns to include |
| `layout` | LayoutConfig | **deprecated** — Always uses stretch layout. |
| `permission` | PermissionConfig |  |
| `tools` | object |  |
| `attachment` | AttachmentConfig | Attachment processing configuration, including image size limits and resizing behavior |
| `enterprise` | object |  |
| `tool_output` | object | Thresholds for truncating tool output. When output exceeds either limit, the full text is written to the truncation directory and a preview is retu... |
| `compaction` | object |  |
| `experimental` | object |  |
