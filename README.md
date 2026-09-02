# Allium Plugin for Claude Code

A Claude Code plugin that gives an agent live access to [Allium](https://www.allium.so/)'s
blockchain data across 150+ chains, together with the skills that teach it to query that
data correctly the first time.

## Install

```
/plugin marketplace add allium-labs/allium-claude-plugin
/plugin install allium@allium-labs
```

## What you get

### Allium MCP server

The plugin connects to Allium's hosted MCP server at `https://mcp-oauth.allium.so` over
OAuth. You are prompted to sign in on first use. Register at
[app.allium.so](https://app.allium.so/) if you do not have an account.

The server provides tools to:

- Search schemas and documentation
- Run SQL and fetch results
- Create, read, and update Explorer queries, visuals, and dashboards
- Browse public Terminal dashboards
- Query Realtime prices, balances, positions, and transactions

### Skills

| Skill | Description |
|-------|-------------|
| `sql-optimization` | SQL performance patterns and chain-specific pitfalls. Required before any SQL |
| `product-guide` | Explorer, Realtime APIs, Datastreams, and Datashares, plus the supported-chains list |
| `dashboard-design` | The `set_dashboard` model, element catalog, and layout rules |
| `explorer-visuals` | Chart types, schemas, and palettes for Explorer query visuals |
| `allium-investigation` | Pick the source, build the method, validate, make calibrated claims |
| `data-matching` | Match a question to the right schema and source before writing SQL |
| `dex-analysis` | DEX and AMM volume, liquidity, and pricing, including double-counting pitfalls |
| `stablecoin-analysis` | Stablecoin supply, transfers, and holder analysis |
| `rwa-analysis` | Tokenized real-world asset supply, holders, and flows |
| `bridge-analysis` | Cross-chain bridge volume and flow analysis |
| `lending-analysis` | Lending protocol deposits, borrows, and liquidations |

`dashboard-design` and `explorer-visuals` fetch their content through `get_skill` at use
time, because those schemas are generated from live API models.

### Agents

| Agent | Description |
|-------|-------------|
| `sql-expert` | Write and optimize queries with joins, CTEs, and window functions |
| `docs-expert` | Answer questions on data models, schemas, and API usage |
| `dashboard-builder` | Build a dashboard from existing Explorer queries |

### Commands

| Command | Description |
|---------|-------------|
| `/allium-query` | Answer a blockchain data question with SQL |

## Example use cases

**Example 1: Answer a metric question**

> "How much DEX volume did Base do last week?"

Finds the right `dex` schema, checks for a pre-aggregated metrics table, writes the query
with a `block_timestamp` window, runs it, and reports the number with the row count and
window behind it.

**Example 2: Locate the data**

> "Which table has ERC-20 transfers with USD amounts already attached?"

Searches schemas and docs, and returns the fully qualified table name, the exact columns,
the grain of the table, and its known coverage gaps.

**Example 3: Check coverage**

> "Does Allium support Monad? How many chains in total?"

Reads the canonical, dated supported-chains list from the `product-guide` skill rather
than answering from model memory.

**Example 4: Reconcile a number that looks wrong**

> "My Uniswap volume is roughly 2x what the public dashboards show. Here's my query."

Works through the usual causes in order — per-hop double-counting on multi-hop swaps,
protocol-vs-project grouping, fee-leg reconstruction — before rewriting anything.

**Example 5: Run a full investigation**

> "How has tokenized RWA treasury supply grown over the past 6 months?"

Checks Terminal for existing coverage, selects the source, builds the method from a small
test up to production scale, validates the result, and makes calibrated claims with the
caveats stated.

**Example 6: Build a dashboard**

> "Turn my stablecoin queries into a dashboard"

Reads the existing Explorer queries, works out which one supports head-to-head
comparison, and builds the dashboard with every number bound to a `query_id`.

**Example 7: Read live data**

> "What's the current USDC balance of this wallet across every chain it's active on?"

Uses the Realtime endpoints for balances and prices instead of querying historical
tables.

**Example 8: Choose a product**

> "We need onchain balances in our app with sub-second latency. Explorer or Realtime?"

Compares the products on their actual latency and delivery characteristics.

## Repository layout

```
.claude-plugin/plugin.json        Plugin manifest
.claude-plugin/marketplace.json   Marketplace entry, for direct installs
.mcp.json                         Allium MCP server
skills/                           11 skills
agents/                           3 agents
commands/                         /allium-query
```

## Credits

- Skills by Allium, with the analysis methodology skills shared from
  [allium-labs/skills](https://github.com/allium-labs/skills)
- MCP server by Allium

## License

MIT. See [LICENSE](LICENSE).
