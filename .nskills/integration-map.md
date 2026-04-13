# Integration Map

How components connect and what data flows between them.

### Erc721-stylus --> Frontend-scaffold

- **Source**: Erc721-stylus (`264a8cb0`)
  - Output ports: NFT Contract (contract)
- **Target**: Frontend-scaffold (`cf0edd37`)
  - Input ports: Contract ABI (contract), Network Config (config)

### Frontend-scaffold --> Wallet-auth

- **Source**: Frontend-scaffold (`cf0edd37`)
  - Output ports: App Context (config)
- **Target**: Wallet-auth (`9b5db22e`)
  
