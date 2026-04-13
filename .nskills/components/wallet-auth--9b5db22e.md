# Wallet Auth

| Field | Value |
|-------|-------|
| Type | `wallet-auth` |
| ID | `9b5db22e` |
| Category | app |
| Tags | auth, wallet, siwe, login, web3 |
| Description | WalletConnect, social login, SIWE |

## Configuration

| Setting | Value |
|---------|-------|
| Provider | rainbowkit |
| Wallet Connect Enabled | Enabled |
| Siwe Enabled | Enabled |
| Social Logins | (none) |
| Session Persistence | Enabled |

## Environment Variables

| Key | Description | Required | Secret | Default |
|-----|-------------|----------|--------|---------|
| `NEXT_PUBLIC_WALLETCONNECT_PROJECT_ID` | WalletConnect Cloud project ID | Yes | No |  |
| `NEXT_PUBLIC_APP_NAME` | Application name for wallet dialogs | No | No | My DApp |

## Scripts

| Name | Command |
|------|---------|
| `wallet:setup` | `echo "Get your WalletConnect Project ID from https://dashboard.reown.com"` |

## Integration Points

**Depends on:**
- Frontend-scaffold (`cf0edd37`)

