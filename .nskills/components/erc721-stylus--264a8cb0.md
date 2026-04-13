# ERC-721 NFT

| Field | Value |
|-------|-------|
| Type | `erc721-stylus` |
| ID | `264a8cb0` |
| Category | contracts |
| Tags | nft, erc721, stylus, arbitrum, collectible |
| Description | Deploy NFT collection on Arbitrum Stylus |

## Configuration

| Setting | Value |
|---------|-------|
| Collection Name | SuperPositionNFT |
| Collection Symbol | SPTNFT |
| Network | arbitrum-sepolia |
| Selected Functions | mint, mint_to, safe_mint, burn |

## Environment Variables

| Key | Description | Required | Secret | Default |
|-----|-------------|----------|--------|---------|
| `NEXT_PUBLIC_NFT_ADDRESS` | Deployed ERC721 NFT address | No | No |  |
| `ERC721_DEPLOYMENT_API_URL` | URL of the ERC721 deployment API | No | No | http://localhost:4001 |

## Scripts

| Name | Command |
|------|---------|
| `deploy:erc721` | `ts-node scripts/deploy-erc721.ts` |
| `nft:info` | `ts-node scripts/nft-info.ts` |

## Documentation

### ERC-721 NFT Collection

# SuperPositionNFT (SPTNFT)

An ERC-721 NFT collection for Arbitrum Sepolia using Stylus.

## Collection Details

- **Name:** SuperPositionNFT
- **Symbol:** SPTNFT
- **Base URI:** https://api.example.com/metadata/
- **Network:** arbitrum-sepolia
- **Features:** ownable, mintable, burnable, pausable

## Deployment

```bash
pnpm deploy:erc721
```

This will deploy the NFT collection and output the contract address.

## Usage

### Get Collection Info

```typescript
import { fetchCollectionInfo } from '@/lib/erc721-nft';

const info = await fetchCollectionInfo();
console.log(info.name, info.symbol, info.totalSupply);
```

### Mint NFT (Owner Only)

```typescript
import { mintNFT } from '@/lib/erc721-nft';

const { hash, tokenId } = await mintNFT('0x...', privateKey);
console.log('Minted NFT #' + tokenId);
```

### Transfer NFT

```typescript
import { transferNFT } from '@/lib/erc721-nft';

await transferNFT('0x...from', '0x...to', 1n, privateKey);
```

## Contract Features

- **ownable**: Enabled
- **mintable**: Enabled
- **burnable**: Enabled
- **pausable**: Enabled


## File Structure

This component would generate the following files:

- `deploy-erc721.ts` (contract-scripts)
- `erc721-nft.ts` (frontend-lib)
- `ERC721NFTPanel.tsx` (frontend-components)

## Integration Points

**Provides to:**
- Frontend-scaffold (`cf0edd37`)

