# RemitLend Technical Wiki

Welcome to the RemitLend Developer Wiki. This documentation provides deep-dives into our system's architecture, smart contracts, and design patterns.

## Technical Deep-Dives

-   [**Soroban Smart Contracts**](Soroban-Smart-Contracts.md): Deep-dive into our Rust contracts, the loan lifecycle state machine, and collateral management.
-   [**Indexer & Synchronization Flow**](Indexer-Sync-Flow.md): How we keep our off-chain PostgreSQL database in sync with the Stellar ledger using a custom event indexer.
-   [**Frontend 'Standard Library'**](Frontend-Design-Patterns.md): Developer guide for our UI components, design patterns, and wallet integration.

## Getting Started

If you are a new contributor, please start with our:
1.  [**CONTRIBUTING.md**](../CONTRIBUTING.md): Professional guidelines, branching model, and environment setup.
2.  [**ARCHITECTURE.md**](../ARCHITECTURE.md): System-level overview and high-level data flows.

## Core Components

-   **Backend**: Express.js, TypeScript, PostgreSQL.
-   **Frontend**: Next.js, Tailwind CSS, Stellar Wallet Kit.
-   **Blockchain**: Soroban (Rust), Stellar SDK.
