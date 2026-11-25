# Allium Supported Chains — Canonical List

**Snapshot date:** 2026-11-11

This is the authoritative, product-segmented list of blockchains Allium
supports. Quote it directly when answering "what chains does Allium
support?" — do not list chains or totals from memory. State which product
the count refers to, and make the headline total match the row count for
that product in this file.

**Sources of truth (regenerate from these when updating this file):**

- Historical data (Explorer, Datashares, Datastreams — one shared data
  platform): <https://docs.allium.so/historical-data/coverage>
- Realtime APIs: <https://docs.allium.so/api/developer/availability> — also
  live via the `get_realtime_supported_chains` tool
  (`/api/v1/supported-chains/realtime-apis/simple`), which is the
  up-to-the-minute source; the Realtime table below is a dated snapshot.

## Headline totals

- **Historical data platform (Explorer / Datashares / Datastreams): 120 chains** (as of 2026-11-11; 26 more are deprecated, listed separately below).
- **Realtime APIs: 22 chains** (as of 2026-11-11; the roster changes over time, so confirm via <https://docs.allium.so/api/developer/availability>).

Ecosystem breakdown (historical): EVM 83, SVM 3, Move 4, Cosmos SDK 9, Bitcoin/UTXO 5, Hyperliquid 1, Lighter 2, Other 13.

Starknet is listed under Other because it runs Cairo, not the EVM, although the docs
coverage matrix tags it EVM.

## Legend

✅ supported · 🌱 beta · — not supported · text = partial
(e.g. "Fungible Only", "ERC Transfers Only", "Traces Only", "On Demand").
Every chain in the Historical table is available in Explorer and via
Datashares/Datastreams; the columns show which enriched schemas are decoded
for that chain. **Status** is the chain's own lifecycle (GA or Beta).
**Realtime** marks chains also served by the Realtime APIs. **Chain ID** is
the identifier used in SQL schemas and API requests.

## Historical data platform — Explorer / Datashares / Datastreams

| Chain | Chain ID | Ecosystem | Status | Raw | Decoded | Transfers | Balances | DEX | Perpetuals | Lending | Staking | NFTs | Bridges | Wallet360 | Realtime |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| Abstract | `abstract` | EVM | GA | ✅ | — | ✅ | ✅ | — | — | — | — | ✅ | ✅ | — | — |
| ApeChain | `apechain` | EVM | GA | ✅ | — | ✅ | Fungible Only | — | — | — | — | ✅ | — | — | — |
| Arbitrum | `arbitrum` | EVM | GA | ✅ | ✅ | ✅ | ✅ | ✅ | 🌱 | ✅ | — | ✅ | ✅ | — | ✅ |
| Arbitrum Nova | `arbitrum_nova` | EVM | GA | ✅ | ✅ | ✅ | — | — | — | — | — | — | — | — | — |
| Arbitrum Sepolia | `arbitrum_sepolia` | EVM | GA | ✅ | — | ✅ | — | — | — | — | — | — | — | — | — |
| Arc | `arc` | EVM | GA | ✅ | ✅ | ✅ | ✅ | ✅ | — | ✅ | — | ✅ | ✅ | — | ✅ |
| Arc Testnet | `arc_testnet` | EVM | Beta | ✅ | ✅ | — | Fungible Only | — | — | — | — | — | — | — | — |
| Astar | `astar` | EVM | GA | ✅ | — | — | — | — | — | — | — | — | — | — | — |
| Avalanche | `avalanche` | EVM | GA | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | — | ✅ | ✅ | — | ✅ |
| Avalanche Fuji | `avalanche_fuji` | EVM | Beta | ✅ | ✅ | ✅ | Fungible Only | — | — | — | — | — | — | — | — |
| Base | `base` | EVM | GA | ✅ | ✅ | ✅ | ✅ | ✅ | — | ✅ | — | ✅ | ✅ | ✅ | ✅ |
| Base Sepolia | `base_sepolia` | EVM | Beta | ✅ | ✅ | ✅ | — | — | — | — | — | — | — | — | — |
| Beacon Chain | `beacon` | EVM | GA | ✅ | — | — | — | — | — | — | — | — | — | — | — |
| Beacon Hoodi | `beacon_hoodi` | EVM | Beta | ✅ | — | — | — | — | — | — | — | — | — | — | — |
| Berachain | `berachain` | EVM | GA | ✅ | — | ✅ | ✅ | ✅ | — | — | — | ✅ | ✅ | — | — |
| BNB Smart Chain | `bsc` | EVM | GA | ✅ | ✅ | ✅ | ✅ | ✅ | — | ✅ | ✅ | ✅ | ✅ | — | ✅ |
| BNB Smart Chain (BSC) Testnet | `bsc_testnet` | EVM | Beta | ✅ | — | ✅ | Fungible Only | — | — | — | — | — | — | — | — |
| BOB | `bob` | EVM | GA | ✅ | ✅ | ✅ | ✅ | ✅ | — | — | — | — | — | — | — |
| Celo | `celo` | EVM | GA | ✅ | ✅ | ✅ | Fungible Only | ✅ | — | ✅ | — | — | — | — | ✅ |
| Celo Sepolia | `celo_sepolia` | EVM | Beta | ✅ | ✅ | — | Fungible Only | — | — | — | — | — | — | — | — |
| Codex | `codex` | EVM | GA | ✅ | ✅ | ✅ | — | — | — | — | — | — | — | — | — |
| Core | `core` | EVM | GA | ✅ | ✅ | ✅ | ✅ | — | — | — | — | — | — | — | — |
| Doge OS Testnet | `doge_os_testnet` | EVM | GA | ✅ | — | — | — | — | — | — | — | — | — | — | — |
| Elysium | `elysium` | EVM | GA | ✅ | ✅ | ✅ | ✅ | ✅ | — | — | — | — | ✅ | — | — |
| Ethereal | `ethereal` | EVM | GA | ✅ | ✅ | ✅ | — | — | — | — | — | — | — | — | — |
| Ethereum | `ethereum` | EVM | GA | ✅ | ✅ | ✅ | ✅ | ✅ | — | ✅ | — | ✅ | ✅ | ✅ | ✅ |
| Ethereum Hoodi | `ethereum_hoodi` | EVM | GA | ✅ | — | ✅ | — | — | — | — | — | — | — | — | — |
| Ethereum Sepolia | `ethereum_sepolia` | EVM | GA | ✅ | ✅ | ✅ | — | — | — | — | — | — | — | — | — |
| Filecoin EVM | `filecoin_evm` | EVM | Beta | ✅ | — | ✅ | — | — | — | — | — | — | — | — | — |
| Flynet | `flynet` | EVM | Beta | ✅ | ✅ | ✅ | Fungible Only | — | — | — | — | — | — | — | — |
| Fraxtal | `fraxtal` | EVM | GA | ✅ | — | ✅ | — | ✅ | — | — | — | — | — | — | — |
| Gnosis | `gnosis` | EVM | GA | ✅ | ✅ | ✅ | — | ✅ | — | ✅ | — | — | — | — | — |
| Gravity | `gravity` | EVM | GA | ✅ | — | — | — | — | — | — | — | — | — | — | — |
| HyperEVM | `hyperevm` | EVM | GA | ✅ | ✅ | ✅ | ✅ | ✅ | — | ✅ | — | ✅ | ✅ | — | ✅ |
| Immutable zkEVM | `imx_zkevm` | EVM | GA | ✅ | — | ERC Transfers Only | NFTs Only | — | — | — | — | — | — | — | — |
| Ink | `ink` | EVM | GA | ✅ | ✅ | ✅ | ✅ | ✅ | — | ✅ | — | — | ✅ | — | — |
| Ink Sepolia | `ink_sepolia` | EVM | Beta | ✅ | ✅ | — | — | — | — | — | — | — | — | — | — |
| Katana | `katana` | EVM | GA | ✅ | ✅ | ✅ | — | — | — | ✅ | — | — | ✅ | — | — |
| Linea | `linea` | EVM | GA | ✅ | ✅ | ✅ | ✅ | ✅ | — | ✅ | — | — | ✅ | — | — |
| Manta Pacific | `manta_pacific` | EVM | GA | ✅ | ✅ | — | — | — | — | — | — | — | — | — | — |
| Mantle | `mantle` | EVM | GA | ✅ | ✅ | ✅ | Fungible Only | ✅ | — | ✅ | — | — | ✅ | — | — |
| MegaETH | `megaeth` | EVM | Beta | ✅ | ✅ | ✅ | Fungible Only | 🌱 | 🌱 | 🌱 | — | — | 🌱 | — | — |
| Metis | `metis` | EVM | GA | ✅ | ✅ | — | — | — | — | — | — | — | — | — | — |
| Mode | `mode` | EVM | GA | ✅ | ✅ | ✅ | — | ✅ | — | — | — | — | ✅ | — | — |
| Monad | `monad` | EVM | GA | ✅ | ✅ | ✅ | ✅ | ✅ | 🌱 | ✅ | ✅ | ✅ | ✅ | — | ✅ |
| Monad Testnet | `monad_testnet` | EVM | GA | ✅ | — | ✅ | ✅ | — | — | — | — | — | — | — | — |
| Mova | `mova` | EVM | GA | ✅ | ✅ | — | Fungible Only | — | — | — | — | — | — | — | — |
| Oasys | `oasys` | EVM | GA | Blocks Transactions and Logs Only | — | ERC Transfers Only | NFTs Only | — | — | — | — | — | — | — | — |
| Optimism | `optimism` | EVM | GA | ✅ | ✅ | ✅ | ✅ | ✅ | — | ✅ | — | ✅ | ✅ | — | ✅ |
| Optimism Sepolia | `optimism_sepolia` | EVM | Beta | ✅ | — | ✅ | Fungible Only | — | — | — | — | — | — | — | — |
| Plasma | `plasma` | EVM | GA | ✅ | ✅ | ✅ | ✅ | ✅ | — | ✅ | — | — | ✅ | — | — |
| Plasma Testnet | `plasma_testnet` | EVM | Beta | ✅ | ✅ | ✅ | Fungible Only | — | — | — | — | — | — | — | — |
| Plume | `plume` | EVM | GA | ✅ | ✅ | ✅ | — | — | — | ✅ | — | — | — | — | — |
| Polygon | `polygon` | EVM | GA | ✅ | ✅ | ✅ | ✅ | ✅ | — | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| Polygon Amoy | `polygon_amoy` | EVM | Beta | ✅ | — | ✅ | Fungible Only | — | — | — | — | — | — | — | — |
| Ritual Testnet | `ritual_testnet` | EVM | Beta | ✅ | — | — | — | — | — | — | — | — | — | — | — |
| Robinhood | `robinhood` | EVM | GA | ✅ | ✅ | ✅ | ✅ | ✅ | — | ✅ | — | ✅ | ✅ | — | ✅ |
| Robinhood Testnet | `robinhood_testnet` | EVM | GA | ✅ | — | ✅ | Fungible Only | — | — | — | — | — | — | — | — |
| Ronin | `ronin` | EVM | GA | ✅ | — | ✅ | ✅ | — | — | — | — | ✅ | — | — | — |
| Rootstock | `rootstock` | EVM | GA | ✅ | — | ✅ | — | — | — | — | — | — | — | — | — |
| Sanko | `sanko` | EVM | GA | ✅ | — | — | — | — | — | — | — | — | — | — | — |
| Scroll | `scroll` | EVM | GA | ✅ | ✅ | ✅ | ✅ | ✅ | — | ✅ | — | — | ✅ | — | — |
| Sei | `sei` | EVM | GA | ✅ | — | ✅ | Fungible Only | — | — | — | — | — | ✅ | — | — |
| Sei Testnet | `sei_testnet` | EVM | Beta | ✅ | — | ✅ | Fungible Only | — | — | — | — | — | — | — | — |
| Seismic Testnet | `seismic_testnet` | EVM | Beta | ✅ | — | — | Fungible Only | — | — | — | — | — | — | — | — |
| Soneium | `soneium` | EVM | GA | ✅ | ✅ | ✅ | ✅ | ✅ | — | ✅ | — | — | ✅ | — | — |
| Sonic | `sonic` | EVM | GA | ✅ | ✅ | ✅ | Fungible Only | ✅ | — | ✅ | — | — | ✅ | — | — |
| Stable | `stable` | EVM | GA | ✅ | ✅ | ✅ | Fungible Only | ✅ | — | ✅ | — | — | ✅ | — | — |
| Stable Testnet | `stable_testnet` | EVM | GA | ✅ | — | — | — | — | — | — | — | — | — | — | — |
| Tempo | `tempo` | EVM | GA | ✅ | ✅ | ✅ | ✅ | ✅ | — | ✅ | — | — | — | — | — |
| Tempo Testnet | `tempo_testnet` | EVM | GA | ✅ | — | ✅ | — | — | — | — | — | — | — | — | — |
| TRON | `tron` | EVM | GA | Blocks Transactions and Logs Only | — | ✅ | Fungible Only | ✅ | — | ✅ | ✅ | — | ✅ | — | — |
| TRON Nile Testnet | `tron_nile` | EVM | Beta | Blocks Transactions and Logs Only | — | Fungible Only | — | — | — | — | — | — | — | — | — |
| Unichain | `unichain` | EVM | GA | ✅ | ✅ | ✅ | ✅ | ✅ | — | ✅ | — | ✅ | ✅ | — | ✅ |
| Unichain Sepolia | `unichain_sepolia` | EVM | Beta | ✅ | — | — | — | 🌱 | — | — | — | — | — | — | — |
| Vana | `vana` | EVM | GA | ✅ | ✅ | ✅ | ✅ | ✅ | — | — | — | — | — | — | — |
| WEMIX | `wemix` | EVM | Beta | ✅ | — | — | — | — | — | — | — | — | — | — | — |
| World Chain | `worldchain` | EVM | GA | ✅ | ✅ | ✅ | ✅ | ✅ | — | ✅ | — | — | ✅ | — | — |
| X Layer | `x_layer` | EVM | GA | ✅ | ✅ | ✅ | ✅ | ✅ | — | ✅ | — | — | — | — | ✅ |
| XDC Network | `xdc_network` | EVM | GA | ✅ | ✅ | ✅ | ✅ | — | — | — | — | — | — | — | ✅ |
| ZKsync | `zksync` | EVM | GA | ✅ | ✅ | ✅ | ✅ | ✅ | — | ✅ | — | — | ✅ | — | ✅ |
| ZkSync Sepolia | `zksync_sepolia` | EVM | Beta | ✅ | ✅ | — | Fungible Only | — | — | — | — | — | — | — | — |
| Zora | `zora` | EVM | GA | ✅ | Traces Only | ✅ | ✅ | ✅ | — | — | — | ✅ | — | — | — |
| Solana | `solana` | SVM | GA | ✅ | On Demand | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | — | ✅ |
| Solana Devnet | `solana_devnet` | SVM | Beta | ✅ | — | — | ✅ | — | — | — | 🌱 | — | — | — | — |
| Solana Testnet | `solana_testnet` | SVM | Beta | ✅ | — | — | — | — | — | — | — | — | — | — | — |
| Aptos | `aptos` | Move | GA | ✅ | — | Fungible Only | Fungible Only | ✅ | — | ✅ | ✅ | — | ✅ | — | — |
| IOTA | `iota` | Move | GA | ✅ | — | — | — | — | — | — | ✅ | — | — | — | — |
| Sui | `sui` | Move | GA | ✅ | — | Fungible Only | ✅ | ✅ | — | ✅ | ✅ | ✅ | ✅ | — | — |
| Sui Testnet | `sui_testnet` | Move | Beta | ✅ | — | — | — | — | — | — | — | — | — | — | — |
| Babylon | `babylon` | Cosmos SDK | GA | ✅ | — | Fungible Only | Fungible Only | — | — | — | — | — | — | — | — |
| Celestia | `celestia` | Cosmos SDK | GA | ✅ | — | — | — | — | — | — | — | — | — | — | — |
| Cosmos | `cosmos` | Cosmos SDK | GA | ✅ | — | Fungible Only | Fungible Only | — | — | — | ✅ | — | — | — | — |
| dYdX | `dydx` | Cosmos SDK | GA | ✅ | — | Fungible Only | Fungible Only | — | — | — | — | — | — | — | — |
| Injective | `injective` | Cosmos SDK | GA | ✅ | — | Fungible Only | Fungible Only | — | — | — | — | — | — | — | — |
| Kava | `kava` | Cosmos SDK | Beta | ✅ | — | — | — | — | — | — | — | — | — | — | — |
| MANTRA | `mantra` | Cosmos SDK | Beta | ✅ | — | — | — | — | — | — | — | — | — | — | — |
| Osmosis | `osmosis` | Cosmos SDK | GA | ✅ | — | ✅ | Fungible Only | — | — | — | — | — | — | — | — |
| Provenance | `provenance` | Cosmos SDK | GA | ✅ | — | Fungible Only | — | ✅ | — | — | — | — | — | — | — |
| Bitcoin | `bitcoin` | Bitcoin/UTXO | GA | ✅ | — | ✅ | ✅ | — | — | — | — | ✅ | — | — | ✅ |
| Bitcoin Cash | `bitcoin_cash` | Bitcoin/UTXO | GA | ✅ | — | — | ✅ | — | — | — | — | — | — | — | — |
| Dogecoin | `dogecoin` | Bitcoin/UTXO | GA | ✅ | — | — | ✅ | — | — | — | — | — | — | — | ✅ |
| Litecoin | `litecoin` | Bitcoin/UTXO | GA | ✅ | — | — | ✅ | — | — | — | — | — | — | — | — |
| Stacks | `stacks` | Bitcoin/UTXO | GA | ✅ | — | — | — | — | — | — | — | — | — | — | — |
| Hyperliquid | `hyperliquid` | Hyperliquid | GA | ✅ | — | ✅ | ✅ | ✅ | ✅ | — | — | — | — | — | ✅ |
| Lighter | `lighter` | Lighter | GA | ✅ | — | — | — | ✅ | ✅ | — | — | — | — | — | — |
| Lighter Robinhood | `lighter_robinhood` | Lighter | GA | ✅ | — | — | — | ✅ | ✅ | — | — | — | — | — | — |
| Canton Network | `canton` | Other | GA | ✅ | — | — | — | — | — | — | — | — | — | — | — |
| Cardano | `cardano` | Other | GA | ✅ | — | — | Fungible Only | — | — | — | — | — | — | — | — |
| Casper Network | `casper` | Other | GA | ✅ | — | Fungible Only | ✅ | ✅ | — | — | ✅ | — | — | — | — |
| Filecoin | `filecoin` | Other | Beta | ✅ | — | Fungible Only | Fungible Only | — | — | — | — | — | — | — | — |
| Hedera | `hedera` | Other | GA | ✅ | — | — | — | — | — | — | — | — | — | — | — |
| NEAR | `near` | Other | GA | ✅ | — | ✅ | Fungible Only | — | — | — | ✅ | ✅ | ✅ | — | ✅ |
| Spark | `spark` | Other | Beta | ✅ | — | — | — | — | — | — | — | — | — | — | — |
| Starknet | `starknet` | Other | GA | ✅ | — | ERC Transfers Only | — | — | — | — | — | — | — | — | — |
| Stellar | `stellar` | Other | GA | ✅ | — | Fungible Only | ✅ | ✅ | — | ✅ | — | ✅ | ✅ | — | ✅ |
| Stellar Testnet | `stellar_testnet` | Other | Beta | ✅ | — | — | — | — | — | — | — | — | — | — | — |
| TON | `ton` | Other | GA | ✅ | — | ✅ | Fungible Only | — | — | — | ✅ | — | — | — | — |
| TON Testnet | `ton_testnet` | Other | Beta | ✅ | — | — | — | — | — | — | — | — | — | — | — |
| XRP Ledger | `xrp_ledger` | Other | GA | ✅ | — | ✅ | — | — | — | — | — | — | — | — | — |

## Realtime APIs

22 chains as of 2026-11-11. The Realtime roster changes over time: confirm
against <https://docs.allium.so/api/developer/availability> or the
`get_realtime_supported_chains` tool.

| Chain | Chain ID | Type | Availability | Endpoint groups |
|---|---|---|---|---|
| Arbitrum | `arbitrum` | EVM | GA | Assets, Balances, Holdings, PnL, Prices, Tokens, Transactions, Wallet |
| Arc | `arc` | EVM | GA | Balances, Tokens, Transactions |
| Avalanche | `avalanche` | EVM | GA | Balances, Holdings, PnL, Prices, Tokens, Transactions, Wallet |
| Base | `base` | EVM | GA | Assets, Balances, Holdings, PnL, Prices, Tokens, Transactions, Wallet |
| Bitcoin | `bitcoin` | bitcoin | GA | Tokens |
| BNB Smart Chain | `bsc` | EVM | GA | Balances, Holdings, PnL, Prices, Tokens, Transactions, Wallet |
| Celo | `celo` | EVM | GA | Balances, Holdings, PnL, Prices, Tokens, Transactions, Wallet |
| Dogecoin | `dogecoin` | bitcoin | GA | Tokens |
| Ethereum | `ethereum` | EVM | GA | Assets, Balances, Holdings, PnL, Prices, Tokens, Transactions, Wallet |
| HyperEVM | `hyperevm` | EVM | GA | Balances, Holdings, Hyperliquid, PnL, Prices, Tokens, Transactions, Wallet |
| Hyperliquid | `hyperliquid` | EVM | GA | Wallet |
| Monad | `monad` | EVM | Beta | Balances, Holdings, PnL, Tokens, Transactions, Wallet |
| NEAR | `near` | near | GA | Balances, Transactions |
| Optimism | `optimism` | EVM | GA | Assets, Balances, Holdings, PnL, Prices, Tokens, Transactions, Wallet |
| Polygon | `polygon` | EVM | GA | Assets, Balances, Holdings, PnL, Prices, Tokens, Transactions, Wallet |
| Robinhood | `robinhood` | EVM | GA | Balances, PnL, Prices, Tokens, Transactions |
| Solana | `solana` | solana | GA | Assets, Balances, Holdings, PnL, Prices, Tokens, Transactions, Wallet |
| Stellar | `stellar` | stellar | GA | Balances, Tokens, Transactions |
| Unichain | `unichain` | EVM | GA | Balances, Holdings, PnL, Prices, Tokens, Transactions, Wallet |
| X Layer | `x_layer` | EVM | Beta | Balances, PnL, Tokens, Transactions, Wallet |
| XDC Network | `xdc_network` | EVM | GA | Balances, Tokens, Transactions |
| ZKsync | `zksync` | EVM | GA | Holdings, PnL, Prices, Tokens |

## Deprecated historical chains

26 chains still appear in the docs but are deprecated. They are not
counted in the historical total. When asked about one, say it is deprecated.

| Chain | Chain ID | Ecosystem |
|---|---|---|
| Aleph Zero | `aleph_zero` | EVM |
| AlienX | `alienx` | EVM |
| B3 | `b3` | EVM |
| Blast | `blast` | EVM |
| Botanix | `botanix` | EVM |
| Degen | `degen` | EVM |
| EDU Chain | `educhain` | EVM |
| Everclear | `everclear` | EVM |
| Fantom | `fantom` | EVM |
| Holesky | `holesky` | EVM |
| Kadena EVM Testnet | `kadena_evm_testnet` | EVM |
| Kinto | `kinto` | EVM |
| Kroma | `kroma` | EVM |
| LogX | `logx` | EVM |
| Polygon zkEVM | `polygon_zkevm` | EVM |
| Proof of Play Apex | `proof_of_play_apex` | EVM |
| Proof of Play Boss | `proof_of_play_boss` | EVM |
| re.al | `real` | EVM |
| Reya | `reya` | EVM |
| Scroll Sepolia | `scroll_sepolia` | EVM |
| Superposition | `superposition` | EVM |
| SX Rollup | `sx` | EVM |
| WINR | `winr` | EVM |
| Xai | `xai` | EVM |
| Dymension | `dymension` | Cosmos SDK |
| Kadena | `kadena` | Other |
