# Changelog

## [0.1.3]

### Added

- `icon` and `privacyPolicyUrl` in `plugin.json` for the directory listing.
- `sql-expert` can list a query's past runs and share an Explorer query.

### Removed

- The `realtime-expert` agent and the Realtime tool from `docs-expert`.
- The API-key setup from the README. The plugin signs in with OAuth only.

### Fixed

- `product-guide`, its supported-chains list, and `sql-optimization` match the skills the
  Allium MCP server serves.

## [0.1.2]

### Added

- `realtime-expert` agent for the Realtime price, wallet, holdings, and Hyperliquid tools.
- `dashboard-builder` finds user dashboards with `search_dashboards` and can schedule their
  queries. `sql-expert` checks the metrics catalog before writing SQL and can schedule
  queries. `docs-expert` can list catalog metrics and live Realtime chain support.
- API-key setup in the README.

### Fixed

- `product-guide` and `sql-optimization` now match the skills the Allium MCP server serves:
  the realtime chain tool is `get_realtime_supported_chains`, and `sql-optimization` adds
  deprecated-table and metrics-catalog guidance.
- Analysis skills no longer name `browse_schemas`, which does not exist.
- `allium-investigation` calls `share_explorer_query` only when it is available.
- Agents use the plugin's MCP tool prefix, `mcp__plugin_allium_allium__`.

## [0.1.1]

### Changed

- Allium MCP server moved to `https://mcp.allium.so`. `https://mcp-oauth.allium.so`
  stops working after 31 October 2026.

## [0.1.0]

### Added

- Allium MCP server (`https://mcp-oauth.allium.so`, OAuth)
- Skills: `sql-optimization`, `product-guide`, `dashboard-design`, `explorer-visuals`,
  `allium-investigation`, `data-matching`, `dex-analysis`, `stablecoin-analysis`,
  `rwa-analysis`, `bridge-analysis`, `lending-analysis`
- Agents: `sql-expert`, `docs-expert`, `dashboard-builder`
- `/allium-query` command
