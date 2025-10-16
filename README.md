# BaseBurn 🔥

A Next.js app that lets you burn USDC on Base Sepolia using Base Account sub-accounts and earn XP!

## Features

- 🔥 Burn USDC to a specific address on Base Sepolia
- 💎 Sub-account creation with automatic spend permissions
- ⛽ **Paymaster support** for sponsored gas fees (no ETH needed!)
- 🎮 XP and leveling system (1 burn = 1 XP, level up every 10 XP)
- 📊 Progress bar and stats tracking
- 💾 Persistent XP storage in localStorage

## Getting Started

### Prerequisites

- Node.js 18+ installed
- A Base Account wallet
- Some USDC on Base Sepolia testnet

### Installation

1. Install dependencies:

```bash
npm install
```

2. **(Optional) Set up Paymaster for sponsored gas:**

Create a `.env.local` file and add your Paymaster service URL:

```env
NEXT_PUBLIC_PAYMASTER_SERVICE_URL=https://api.developer.coinbase.com/rpc/v1/base-sepolia/YOUR_API_KEY
```

See [PAYMASTER_SETUP.md](./PAYMASTER_SETUP.md) for detailed setup instructions.

**Without a Paymaster:** Users will need ETH in their sub-account for gas fees.
**With a Paymaster:** Gas fees are sponsored - users only need USDC! ✨

3. Run the development server:

```bash
npm run dev
```

4. Open [http://localhost:3001](http://localhost:3001) in your browser

## How It Works

1. **Connect**: Click "Connect & Start Burning" to connect your Base Account
2. **Sub-Account**: A sub-account will be created automatically for this app
3. **Burn**: Click the burn button to send 0.01 USDC to the burn address
4. **Level Up**: Each burn earns you 1 XP. Collect 10 XP to level up!

## Configuration

- **Burn Address**: `0x290214A838353fA1250c0A80b83bD6DA23985B1a`
- **USDC Address**: `0x036CbD53842c5426634e7929541eC2318f3dCF7e` (Base Sepolia)
- **Burn Amount**: 0.01 USDC per transaction
- **Chain**: Base Sepolia

## Technologies Used

- Next.js 14
- Base Account SDK
- Viem
- TypeScript
- React

## Note

This is a demo/burner project for testing Base Account sub-accounts functionality.

